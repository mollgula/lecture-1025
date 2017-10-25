# テクノロジー（藤原）10/25授業

```
(ここに実行ログをコピペする)
mollgula:~/workspace (master) $ pry
[1] pry(main)> puts "こんにちは"
こんにちは
=> nil
[2] pry(main)> print "こんにちは"
こんにちは=> nil
[3] pry(main)> p "こんにちは"
"こんにちは"
=> "こんにちは"
[4] pry(main)> message = "こんにちは"
=> "こんにちは"
[5] pry(main)> p message
"こんにちは"
=> "こんにちは"
[6] pry(main)> puts  message
こんにちは
=> nil
[7] pry(main)> num = 123
=> 123
[8] pry(main)> puts num
123
=> nil
[9] pry(main)> puts message.length
5
=> nil
[10] pry(main)> 1234.class
=> Integer
[11] pry(main)> class.class
SyntaxError: unexpected '.'
class.class
      ^
[11] pry(main)> (3.141519).class
=> Float
[12] pry(main)> (class).class
SyntaxError: unexpected ')'
(class).class
       ^
[12] pry(main)> MATH.PI
NameError: uninitialized constant MATH
Did you mean?  Math
from (pry):12:in `__pry__'
[13] pry(main)> Math::PI
=> 3.141592653589793
[14] pry(main)> hello = "こんにちは"
=> "こんにちは"
[15] pry(main)> by = "さようなら"
=> "さようなら"
[16] pry(main)> puts hello + "," + by                                                                                                               
こんにちは,さようなら
=> nil
[17] pry(main)> name = "藤原"
=> "藤原"
[18] pry(main)> puts "#{name}さん,konnnitiha"
藤原さん,konnnitiha
=> nil
[19] pry(main)> puts "#{name}さん,こんにちは"
藤原さん,こんにちは
=> nil
[20] pry(main)> puts "\nさようなら\n"

さようなら
=> nil
[21] pry(main)> a = 4, b = "9"
=> [4, "9"]
[22] pry(main)> puts a + b
TypeError: no implicit conversion of String into Array
from (pry):22:in `__pry__'
[23] pry(main)> puts a.to_i + b                                                                                                                     
NoMethodError: undefined method `to_i' for [4, "9"]:Array
Did you mean?  to_s
               to_a
               to_h
from (pry):23:in `__pry__'
[24] pry(main)> puts a.to_s + b                                                                                                                     
[4, "9"]9
=> nil
[25] pry(main)> a = 4
=> 4
[26] pry(main)> b = "9"
=> "9"
[27] pry(main)> puts a + b 
TypeError: String can't be coerced into Integer
from (pry):27:in `+'
[28] pry(main)> puts a.to_s + b
49
=> nil
[29] pry(main)> puts (a.to_s + b).class                                                                                                             
String
=> nil
[30] pry(main)> puts a + b.to_i 
13
=> nil
[31] pry(main)> puts (a + b.to_i).class
Integer
=> nil
[32] pry(main)> animals = %w(cat, dog, bard)
=> ["cat,", "dog,", "bard"]
[33] pry(main)> animals[0]
=> "cat,"
[34] pry(main)> animals[1]
=> "dog,"
[35] pry(main)> animals[2]
=> "bard"
[36] pry(main)> animals[3] = aligaer
NameError: undefined local variable or method `aligaer' for main:Object
from (pry):36:in `__pry__'
[37] pry(main)> animals[0] = human 
NameError: undefined local variable or method `human' for main:Object
from (pry):37:in `__pry__'
[38] pry(main)> alimals
NameError: undefined local variable or method `alimals' for main:Object
Did you mean?  animals
from (pry):38:in `__pry__'
[39] pry(main)> p animals
["cat,", "dog,", "bard"]
"human"
=> "human"
[42] pry(main)> p animals
["human", "dog,", "bard"]
=> ["human", "dog,", "bard"]
[43] pry(main)> animals.push = "jack"                                                                                                               
NoMethodError: undefined method `push=' for ["human", "dog,", "bard"]:Array
Did you mean?  push
from (pry):43:in `__pry__'
[44] pry(main)> animals.push("jack")
=> ["human", "dog,", "bard", "jack"]
[45] pry(main)> animals.pop
=> "jack"
[46] pry(main)> animals.pop[2]
=> "r"
[47] pry(main)> animals.serach("jack")
NoMethodError: undefined method `serach' for ["human", "dog,"]:Array
Did you mean?  each
from (pry):47:in `__pry__'
[48] pry(main)> animals.serach("jack")
NoMethodError: undefined method `serach' for ["human", "dog,"]:Array
Did you mean?  each
from (pry):48:in `__pry__'
[49] pry(main)> name = []
=> []
[50] pry(main)> name.enpty?
NoMethodError: undefined method `enpty?' for []:Array
Did you mean?  empty?
from (pry):50:in `__pry__'[51] pry(main)> name.empty?                                                                                                                         
=> true
[52] pry(main)> name.length
=> 0
[53] pry(main)> name = %w(jack, joun, alex)
=> ["jack,", "joun,", "alex"]
[54] pry(main)> p name
["jack,", "joun,", "alex"]
=> ["jack,", "joun,", "alex"]
[55] pry(main)> p name.length
3
=> 3
[56] pry(main)> color = %w()
=> []
[57] pry(main)> color.empty?
=> true
[58] pry(main)> color.length
=> 0
[59] pry(main)> color = %w(red, green, blue)
=> ["red,", "green,", "blue"]
[60] pry(main)> num = []
=> []
[61] pry(main)> nums = %w()
=> []
[62] pry(main)> nums = %w(1, 10, 100, 1000)
=> ["1,", "10,", "100,", "1000"]
[63] pry(main)> a = true
=> true
[64] pry(main)> b = 2
=> 2
[65] pry(main)> c = hello 
=> "こんにちは"
[66] pry(main)> if true 
[66] pry(main)*   "a" 
[66] pry(main)* end  
=> "a"
[67] pry(main)> require 'mail '
LoadError: cannot load such file -- mail 
from /usr/local/rvm/rubies/ruby-2.4.0/lib/ruby/2.4.0/rubygems/core_ext/kernel_require.rb:55:in `require'
[68] pry(main)> name_and_address = { name: takahashi, address = 000-0000-0000 }
SyntaxError: unexpected '}', expecting =>
shi, address = 000-0000-0000 }
                              ^
[68] pry(main)> name_and_address = { name: takahashi, address: = 000-0000-0000 }                                                                    
SyntaxError: unexpected '}', expecting end-of-input
hi, address: = 000-0000-0000 }
                              ^
[68] pry(main)> name_and_address = { name: "takahashi", address: = "000-0000-0000" }                                                                
SyntaxError: unexpected '}', expecting end-of-input
, address: = "000-0000-0000" }
                              ^
[68] pry(main)> name_and_address = { name: "takahashi", address: "000-0000-0000" }
=> {:name=>"takahashi", :address=>"000-0000-0000"}
[69] pry(main)> puts :name
name
=> nil
[70] pry(main)> puts name:
[70] pry(main)* 
[70] pry(main)* 
[70] pry(main)* end
SyntaxError: unexpected keyword_end
[70] pry(main)> name_and_address.each do |name, address|
[70] pry(main)*   puts "名前は#{name},電話番号は#{address}です."
[70] pry(main)* end  
名前はname,電話番号はtakahashiです.
名前はaddress,電話番号は000-0000-0000です.
=> {:name=>"takahashi", :address=>"000-0000-0000"}
[71] pry(main)> class DB
[71] pry(main)*   def initialize(yourname = name)
[71] pry(main)*     @name = name 
[71] pry(main)*   end  
[71] pry(main)*   
[71] pry(main)*   def DB1
[71] pry(main)*     puts "#{@name}はスーパーサイヤ人になった"
[71] pry(main)*   end  
[71] pry(main)*   
[71] pry(main)*   def DB2
[71] pry(main)*     puts "#{@name}はスーパーサイヤ人2になった"
[71] pry(main)*   end  
[71] pry(main)*   
[71] pry(main)*   def DB3 
[71] pry(main)*     puts "#{@name}はスーパーサイヤ人3になった"
[71] pry(main)*   end  
[71] pry(main)* end  
=> :DB3
[72] pry(main)> hirose = DB.new("Hirose")
NameError: undefined local variable or method `name' for #<DB:0x00000002a3a3c0>
from (pry):77:in `initialize'
[73] pry(main)> hirose = DB.new
NameError: undefined local variable or method `name' for #<DB:0x00000002a09bd0>
from (pry):76:in `initialize'
[74] pry(main)> class DB
[74] pry(main)*   def initialize(myname = name)  
[74] pry(main)*     @name = myname    
[74] pry(main)*   end  
[74] pry(main)*   
[74] pry(main)*   def DB1  
[74] pry(main)*     puts "#{@name}はスーパーサイヤ人1になった"    
[74] pry(main)*   end  
[74] pry(main)*   
[74] pry(main)*   def DB2 
[74] pry(main)*     puts "#{@name}はスーパーサイヤ人2になった"
[74] pry(main)*   end  
[74] pry(main)*   
[74] pry(main)*   def BD3
[74] pry(main)*     puts "#{@name}はスーパーサイヤ人3になった"    
[74] pry(main)*   end  
[74] pry(main)*   
[74] pry(main)* end  
=> :BD3
[75] pry(main)> hirose = DB.new
NameError: undefined local variable or method `name' for #<DB:0x00000002983288>
from (pry):95:in `initialize'
[76] pry(main)> hirose = DB.new("Hirose")
=> #<DB:0x00000002940aa0 @name="Hirose">
[77] pry(main)> hirose.DB1
Hiroseはスーパーサイヤ人1になった
=> nil
[78] pry(main)> hirose.DB2
Hiroseはスーパーサイヤ人2になった
=> nil
[79] pry(main)> hirose.DB3
Hiroseはスーパーサイヤ人3になった
=> nil
[80] pry(main)> itihara = DB.new("ittiy")
=> #<DB:0x00000002140698 @name="ittiy">
[81] pry(main)> itihara.DB1
ittiyはスーパーサイヤ人1になった
=> nil
[82] pry(main)> itihara.DB1
ittiyはスーパーサイヤ人1になった
=> nil
[83] pry(main)> itihara.DB2
ittiyはスーパーサイヤ人2になった
=> nil
[84] pry(main)> itihara.DB3
ittiyはスーパーサイヤ人3になった
=> nil
[85] pry(main)> 

```
