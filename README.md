# absl.flags
	import tensorflow as tf
	FLAGS = tf.app.flags.FLAGS
	tf.app.flags.DEFINE_string('absl_flags_ex', 'start','ex')
	tf.app.flags.DEFINE_integer('int_a', 0, 'Number')
	tf.app.flags.DEFINE_boolean('flag', False, 'bppl')
	#name default description 
	print(FLAGS.int_a)
使用 python absl_flags_ex.py --int_a 1

# argparse.ArgumentParser()
	import argparse
	parser = argparse.ArgumentParser()#创建一个解析对象
	parser.add_argument('--int_a', type=int, default=128)#向该对象中添加你要关注的命令行参数和选项
	parser.add_argument('--string', type=str, default='string')
	parser.add_argument('--flag', type=bool, default=True)
	#name or flags...    - 必选参数名或者可选参数标识符，它必须作为add_argument()方法的第一个参数。
	#action         - 表示值赋予键的方式，这里用到的是bool类型，action意思是当读取的参数中出现指定参数的时候的行为
	#help       - 参数的说明信息
	#type      - 指定命令行参数数据类型
	#choices    - 说明命令行参数的取值范围，它的值一般是一个列表。choices列表中元素的类型应该与type批定的类型相兼容
	#default   - 必选参数和可选的参数的默认值。
	parser=parser.parse_args()
	print(parser.int_a,parser.string,parser.flag)
使用 python argparse_ex.py --int_a 1

