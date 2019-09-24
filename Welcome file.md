---


---

<p>El programa lo que hace es modificar el color de la pantalla mediante un botón, cuando se presiona dicho botón el color cambia de rojo azul y de azul a rojo</p>
<p><img src="https://lh3.googleusercontent.com/KazBkJFswBr_rSW3Vq6ZzjIyMW3nlfbvCqJojv9fBwGtyA4fnhJtP9FKuGwbx3exu-2Qx4vmUyU" alt="enter image description here"><br>
package com.example.changecolors;</p>
<p>import androidx.appcompat.app.AppCompatActivity;<br>
import androidx.constraintlayout.widget.ConstraintLayout;<br>
import android.graphics.Color;<br>
import android.graphics.drawable.ColorDrawable;<br>
import android.os.Bundle;<br>
import android.view.View;<br>
import android.widget.Button;<br>
//Aqui se estan declarando las librerias a usar<br>
public class MainActivity extends AppCompatActivity {</p>
<pre><code>@Override  
</code></pre>
<p>protected void onCreate(Bundle savedInstanceState) {<br>
super.onCreate(savedInstanceState);<br>
setContentView(R.layout.activity_main);<br>
ConstraintLayout bgElement = findViewById(R.id.activity_main);<br>
bgElement.setBackgroundColor(Color.RED);<br>
myButtonListenerMethod();<br>
}  // en esta parte se le esta asignando el color al background de la app,</p>
<pre><code>public void myButtonListenerMethod()  
{  
    Button button = findViewById(R.id.button);  
    button.setOnClickListener(new View.OnClickListener() {  
        @Override  
</code></pre>
<p>public void onClick(View v) {<br>
ConstraintLayout bgElement =<br>
findViewById(R.id.activity_main);<br>
int color = ((ColorDrawable)<br>
bgElement.getBackground()).getColor();<br>
if (color == Color.RED)<br>
bgElement.setBackgroundColor(Color.BLUE);<br>
else<br>
bgElement.setBackgroundColor(Color.RED);</p>
<pre><code>        }  //en esta parte se le dio funcionalidad al boton para cuando sea presionado si detecta que el bacgroun es color rojo lo cambie a azul y si esta azul que lo regrese a color rojo
    });  

}  
</code></pre>
<p>}</p>

