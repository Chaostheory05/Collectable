# Collectable
//This code is from Epitome's tutorial https://www.youtube.com/watch?v=b8YUfee_pzc&t=23003s

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Collectable : Collidable {

	protected bool collected;
	protected override void OnCollide(Collider2D coll)
	{
		if (coll.name == "Player")
			OnCollect ();
	}
	protected virtual void OnCollect()
	{
		collected = true;
	}
}
