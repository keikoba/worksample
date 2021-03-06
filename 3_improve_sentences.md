selfはインスタンスオブジェクト自身を指しています。クラスの中でインスタンスオブジェクトを呼び出す際やそのインスタンスオブジェクトを呼び出す際は、selfを使用します。

# selfについての大まかな説明  
- self自身は変数のひとつ  
- selfはあるなんらかのオブジェクト（インスタンス）を参照する「指示語」のようなもの  

# 以下のコードの例を見てみましょう！  

    class Dogs  

        p self　#=> Dogs  

        def run  
        　p self  #=> #<Dogs:0x0000000005204f40>  
        　puts 'run run run!' #=> run run run!  

      　end  
    end  
    Dogs.new.run  

## この結果から見ると…  

- class定義内の`self`はClassを返す。（Rubyではclassもオブジェクトのひとつです。）  
- メソッド定義内の`self`はメソッドを呼び出した時のオブジェクト（インスタンス）を返す。    

以上のことがわかります。図1を参照してイメージをつかんでください。   
図1　https://github.com/keikoba/worksample/blob/keikoba-branch1/self%20chart1.pdf

# 次のコードを見て、更に理解を深めましょう！　　

    class Dogs

       def self.colors
        [:black, :brown, :white, :mixed]  

       end  
    end  
    p Dogs.colors  
　　　
   
- このコードの場合、`self`はクラス名（オブジェクト名）の`Dogs`を指します。`Dogs`の`colors`は配列の中の4色がある、という意味コードになります。  図2を参照して確認してみましょう。  
図2　https://github.com/keikoba/worksample/blob/keikoba-branch1/self%20chart2.pdf

　　　　
# まとめ  
このことから、`self`はクラスを含むオブジェクトを指します。どのオブジェクトを指しているかは、その`self`がある場所に依存しますので注意しましょう。   


