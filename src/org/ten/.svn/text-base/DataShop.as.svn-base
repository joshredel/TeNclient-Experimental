package org.ten
{
	import mx.collections.ArrayCollection;

	[Bindable]
	/**
	 * DataShop provides singleton access to all data
	 * and services used throughout the system.
	 */
	public final class DataShop {
		/**************************
		 * Singleton enforcement
		 **************************/
		/**
		 * The reference to the single instance of this class.
		 */
		private static const _instance:DataShop = new DataShop(SingletonEnforcer);
		
		/**
		 * The single instance of this class.
		 * 
		 * @internal
		 * Returns the instance if it has been created, otherwise 
		 * it creates the instance.
		 */
		public static function get instance():DataShop {
			// return the single instance
			return _instance;
		}
		
		/**
		 * Constructor.
		 * Loads all of the classes so they are typeable via AMF.
		 * Prepares all of the services.
		 */
		public function DataShop(access:Class) {
			// require the passing of a SingletonEnforcer
			// because no outside class can use it, so only here 
			// can an instance be created and we can manage it
			if(access != SingletonEnforcer) {
				throw new Error("Singleton enforcement failed.  Use DataShop.instance");
			}
		}
		
		
		public var slides:ArrayCollection = new ArrayCollection(["1.jpg", 
																 "2.jpg", 
																 "3.jpg", 
																 "4.jpg", 
																 "5.jpg", 
																 "6.jpg"]);
	}
}

// by using a class here, no outide class can create
// a new DataShop because it is required in the constructor
class SingletonEnforcer {}