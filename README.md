La prueba consta en la operación básica de 2 números, dentro de la activity colocamos las variables y el spinner imprimir el resultado.

package com.example.prueba_calculadora

import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.widget.ArrayAdapter
import android.widget.Button
import android.widget.EditText
import android.widget.Spinner
import android.widget.TextView
import java.lang.Exception

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)


        val n1 = findViewById<EditText>(R.id.txt_1)
        val n2 = findViewById<EditText>(R.id.txt_2)
        val respuesta = findViewById<TextView>(R.id.txt_respuesta)
        val spinner= findViewById<Spinner>(R.id.spr_1)
        val btn_operar = findViewById<Button>(R.id.btn_ok)


        val lista = arrayOf("sumar", "restar", "multiplicar", "dividir")
        val adaptador1 = ArrayAdapter<String>(this, android.R.layout.simple_spinner_item, lista)
        spinner.adapter = adaptador1
        btn_operar.setOnClickListener {
            when (spinner.selectedItem.toString()) {

                    "sumar" -> respuesta.text =
                    "Resultado: ${n1.text.toString().toInt() + n2.text.toString().toInt()}"

                    "restar" -> respuesta.text =
                    "Resultado: ${n1.text.toString().toInt() - n2.text.toString().toInt()}"

                    "multiplicar" -> respuesta.text =
                    "Resultado: ${n1.text.toString().toInt() * n2.text.toString().toInt()}"

                    "dividir" -> respuesta.text =
                    "Resultado: ${n1.text.toString().toInt() / n2.text.toString().toInt()}"


            }
            
            
        }

        }
        
    }
    
    ![image](https://github.com/ArielVilcaguano/Prueba-parcial-calculadora/assets/133244467/553cd3af-b8bc-4165-b681-6b0f159c6705)

    
    
   

