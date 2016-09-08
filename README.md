# SelfieShare
Repo following Project 25: Selfie Share: MCBrowserViewController and MCSession at Hacking with Swift.  The goal is to practice collection views, image pickers, GCD, and learn about the multipeer connectivity network that creates an ad-hoc network to send data between users.

## Concepts learned/practiced
* Learned:
  * Multipeer Connectivity Network
    * ```MCSession``` - manager class handling multipeer connectivity
    * ```MCBrowserViewController``` - helps search for existing sessions and allowing users to join
    * ```MCPeerID``` - unique ID for each user in a session
    * ```MCAdvertiserAssistant``` - used when creating session, broadcasts out open sessions and handling invitations
* Practiced:
  * Collection Views
    * Protocols:
      * ```UICollectionViewDataSource``` protocol
      * ```UICollectionViewDelegate``` protocol
    * Methods:
      * ```numberOfItemsInSection``` method on ```collectionView``` class
      * ```cellForItemAtIndexPath``` method on ```collectionView``` class
  * Image Picker with the ```UIImagePickerController``` class
    * Protocols:
      * ```UIImagePickerControllerDelegate``` protocol
      * ```UINavigationControllerDelegate``` protocol (needed for image picker to work)
    * Methods:
      * The ```didFinishPickingMediaWithInfo``` method on ```imagePickerController```
      * The ```imagePickerControllerDidCancel``` method and calling ```dimissViewControllerAnimated``` method to cancel out of the Image Picker
  * Grand Central Dispatch(GCD)
    * Example:
    ```Swift
    dispatch_async(dispatch_get_main_queue()) { [unowned self] in
      self.images.insert(image, atIndex: 0)
      self.collectionView.reloadData()
    }
    ```

## Attributions
[Project 25: Selfie Share: MCBrowserViewController and MCSession](https://www.hackingwithswift.com/read/25/overview)
