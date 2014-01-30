MySQL android オープンライブラリ

http://dev.mysql.com/downloads/connector/j/ 

	/* クラスをインポートする */
	import java.sql.*;

	public class MysqlTest {
  		public static void main(String[] args) {
    	try {
      		/* ドライバクラスをロードする */
      		Class.forName("com.mysql.jdbc.Driver"); 

      /*
       * データベースに接続する
       * この場合は
       *   ホスト名      :localhost
       *   データベース名:test
       *   ユーザ名      :user
       *   パスワード    :password
       * とする
       */
      String url = "jdbc:mysql://localhost/test";
      String user="username";
      String pass ="password";
      Connection con = DriverManager.getConnection(url,user,pass);

      /*
       * 中略
       * SQLのクエリ実行，結果の処理などを記述
       */

      /* データベース切断 */
      con.close();
    } catch (Exception e) {
      e.printStackTrace();
    }   
 	 }   
	}