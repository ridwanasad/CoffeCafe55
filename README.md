# CoffeCafe55
package com.example.coffecafe;

import android.os.Bundle;

import androidx.fragment.app.Fragment;

import android.view.LayoutInflater;
import android.view.View;
import android.view.ViewGroup;
import android.widget.EditText;
import android.widget.Toast;


/**
 * A simple {@link Fragment} subclass.
 */
public class AddDrinksFragment extends Fragment {
    private  AddDrinks, Descriptionid, Sizeid;
    private Button BnSave;
    public AddDrinksFragment() {
        // Required empty public constructor
    }


    @Override
    public View onCreateView(LayoutInflater inflater, ViewGroup container,
                             Bundle savedInstanceState) {
        // Inflate the layout for this fragment
        View view = inflater.inflate(R.layout.fragment_add_drinks, container, false);

        AddDrinks = view.findViewById(R.id.ViewAddDrinks.id);
        Descriptionid= view.findViewDescriptionid(R.id.ViewDescriptionidid);
        Sizeid = view.findSizeid(R.id.Sizeid.id);
        BnSave = view.findViewById(R.id.Sizeid);


        BnSave.setOnClickListener(New View.OnClickListener() {

            @Override
            public void OnClick (View view) {

        int AddDrinks = integer.parseInt(AddDrinks.toString());
        String Descriptionid = Descriptionid().toString();
        String Sizeid = Sizeid().toString();

        Drinks drinks = new Drinks ();
        Drinks.setAddDrinks();
        Drinks.setDescriptionid();
        Drinks.setSizeid();

        MainActivity.DunkinDatabase.myDao().addAllMyDrinks();

                Toast.makeText(GetActivity(), "Drinks added succesfully", Toast.LENGTH_SHORT).show();

                AddDrinks.setText("");
                Descriptionid.setText("");
                Sizeid.setText("");


    }

    });

    return view;
        }
}
