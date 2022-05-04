# examhamad

class customAdapter(context: Context,private val name: Array<out String>,private val image : Array<Int>) :
    ArrayAdapter<String>(context, R.layout.forma, name) {
    override fun getView(position: Int, convertView: View?, parent: ViewGroup): View {
        val l:LayoutInflater= LayoutInflater.from(context)
        val customView:View= l.inflate(R.layout.forma,parent,false)
        customView.textView.text = name[position]
        customView.imageView.setImageResource(image[position])

        return customView
    }
}
  
