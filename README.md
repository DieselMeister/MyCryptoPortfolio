# MyCryptoPortfolio

Manages your crypto portfolio on your phone and shows changes to the last rate update.

This app is written in F#, Xamarin and Xamarin.Elmish. (awesome tools)

It's under the MIT Licence.

I use [cryptocompare.com]() to get the current rates and the available symbols for all the crypto currencies. Thanks to these guys. You are awesome.

There is another App named MyCryptoPortfolio in the Windows App Store. The current Version is a rewrite and redesign in F#.

Have fun.

Btw. Please note, that I am using Exceptions in my service code. The first approache was the using of Result. But I ran into a strange error on debugging on my Huawei P20.

The function in the service file return correctly Async<Result<ExRate list, string>>. But the consuming function App.fs -> getRates, gets a strange error message, something with Argument bla, and on "Ok x" x is an integer. So I change to the exception thingy.


# Updates

- 2018-08-30: Fixed the busy state spinner disapears before loading of rates is complete. Introducing a ofAsyncBatchMsg Cmd extension to handle multiple messages after a async task is done. 
- 2018-08-20: After the awesome insperation of https://github.com/TimLariviere/ElmishContacts, 
  I have introduce external command to seperate the pages into their own modules and to composite 
  them in the App.fs like Tim it does. Thanks Tim.

# Description of the App


![image1](docimages/Description_1.png)

![image2](docimages/Description_2.png)

![image3](docimages/Description_3.png)


