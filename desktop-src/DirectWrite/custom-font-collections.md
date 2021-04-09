---
title: Пользовательские коллекции шрифтов (Windows 7/8)
description: DirectWrite предоставляет доступ к коллекции системных шрифтов с помощью метода Идвритефактори Жетсистемфонтколлектион.
ms.assetid: ec892904-6778-4fbd-93b4-62d0db5b82ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39aa764330f27b72051ef682c6ce5f1176c42c7d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792661"
---
# <a name="custom-font-collections-windows-78"></a>Пользовательские коллекции шрифтов (Windows 7/8)

[DirectWrite](direct-write-portal.md) предоставляет доступ к коллекции системных шрифтов с помощью метода [**Идвритефактори:: жетсистемфонтколлектион**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . Это наиболее часто используемая коллекция шрифтов. Однако некоторые приложения должны использовать шрифты, которые не установлены в системе, например из файлов шрифтов или шрифтов, внедренных в приложение.

Если нужные шрифты не находятся в коллекции системных шрифтов, можно создать пользовательскую коллекцию шрифтов, производную от [**идвритефонтколлектион**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection).

Этот обзор состоит из следующих частей.

-   [Регистрация и Отмена регистрации загрузчика коллекции шрифтов](#registering-and-unregistering-a-font-collection-loader)
-   [идвритефонтколлектионлоадер](#idwritefontcollectionloader)
-   [идвритефонтфилинумератор](#idwritefontfileenumerator)
-   [креатекустомфонтфилереференце](#createcustomfontfilereference)
-   [идвритефонтфилелоадер](#idwritefontfileloader)
-   [идвритефонтфилестреам](#idwritefontfilestream)

## <a name="registering-and-unregistering-a-font-collection-loader"></a>Регистрация и Отмена регистрации загрузчика коллекции шрифтов

Вы регистрируете загрузчик коллекции шрифтов с помощью метода [**идвритефактори:: регистерфонтколлектионлоадер**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontcollectionloader) и передаете ему интерфейс [**идвритефонтколлектионлоадер**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) , реализованный приложением как одноэлементный объект. Этот объект будет загружать шрифты при запросе пользовательской коллекции. И коллекция системных шрифтов, и пользовательские коллекции шрифтов кэшируются, поэтому шрифты загружаются только один раз.

Загрузчик коллекции шрифтов должен быть выгружен в конечном итоге с помощью [**идвритефактори:: унрегистерфонтколлектионлоадер**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader).

> [!Note]  
> Регистрация загрузчика коллекции шрифтов добавляет к счетчику ссылок; не вызывайте [**унрегистерфонтколлектионлоадер**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader) из деструктора, иначе не будет отменена регистрация объекта загрузчика коллекции.

 

## <a name="idwritefontcollectionloader"></a>идвритефонтколлектионлоадер

Вы создадите объект [**идвритефонтфилинумератор**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) с помощью [**Идвритефактори:: креатекустомфонтколлектион**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) и передаем ему ключ, определяемый приложением. Ключ является указателем void, а тип данных, формат и значение определяются приложением и являются непрозрачными для системы шрифтов.

В то время как ключ может быть любым, [DirectWrite](direct-write-portal.md) требует, чтобы каждый ключ был одновременно:

-   Уникальный для одной коллекции шрифтов в пределах области загрузчика.
-   Допустимо, пока не будет отменена регистрация загрузчика с помощью фабрики.

Когда вызывается метод [**креатекустомфонтколлектион**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) , [DirectWrite](direct-write-portal.md) обращается к интерфейсу [**идвритефонтколлектионлоадер**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) , реализованному в виде одноэлементного объекта приложения. Метод обратного вызова [**идвритефонтколлектионлоадер:: креатинумераторфромкэй**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) используется DirectWrite для получения объекта [**идвритефонтфилинумератор**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) , реализованного приложением. Объект [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) , который используется для создания коллекции, передается этому методу и должен использоваться перечислителем файла шрифта для создания объектов [**идвритефонтфиле**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) , которые должны быть добавлены в коллекцию.

Ключ, переданный этому методу, определяет коллекцию шрифтов и является тем же ключом, который передается в [**креатекустомфонтколлектион**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection).

## <a name="idwritefontfileenumerator"></a>идвритефонтфилинумератор

Определяемый приложением объект [**идвритефонтфилинумератор**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) , созданный методом [**креатинумераторфромкэй**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) , используется для перечисления файлов шрифтов в коллекции, создания объекта [**идвритефонтфиле**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) для каждого файла. Метод [**идвритефонтфилинумератор:: MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) изменяет расположение на следующий файл шрифта. Если в позиции есть файл, для *хаскуррентфиле* будет задано **значение true**. В противном случае ему будет присвоено значение **false** , и метод возвратит **S \_ ОК**.

> [!Note]  
> Перечислитель файла шрифта должен начинаться с позиции перед первым элементом и дополнительно при первом вызове [**MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext).

 

Объект [**идвритефонтфиле**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) выводится методом [**Идвритефонтфилинумератор:: жеткуррентфонтфиле**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) . Если в текущей позиции нет файла шрифта, поскольку метод [**MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) еще не был вызван или хаскуррентфиле был установлен в **значение false**, то **жеткуррентфонтфиле** возвратит **E \_ Fail**.

## <a name="createcustomfontfilereference"></a>креатекустомфонтфилереференце

Выходные данные объекта [**идвритефонтфиле**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) с помощью [**жеткуррентфонтфиле**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) можно создать, вызвав [**идвритефактори:: креатекустомфонтфилереференце**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference). Ключ ссылки на файл шрифта определяет определенную ссылку на файл шрифта и должен быть уникальным в пределах загрузчика файлов шрифтов, который будет загружать файл.

## <a name="idwritefontfileloader"></a>идвритефонтфилелоадер

Метод [**креатекустомфонтфилереференце**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) принимает объект [**идвритефонтфилелоадер**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) , реализованный приложением, которое используется для загрузки шрифта. Методу обратного вызова [**идвритефонтфилелоадер:: креатестреамфромкэй**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) передается ключ и выводится объект [**идвритефонтфилестреам**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) .

## <a name="idwritefontfilestream"></a>идвритефонтфилестреам

Объект [**идвритефонтфилестреам**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) , реализованный приложением, предоставляет данные файла шрифта для ссылки на файл шрифта из пользовательского загрузчика файлов шрифтов. Вместе с размером файла и временем последней записи он предоставляет метод ([**реадфилефрагмент**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment)) для получения фрагментов файлов, которые должны быть скомпилированы в объект [**идвритефонтфиле**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) .

> [!Note]  
> Реализации [**реадфилефрагмент**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment) должны возвращать ошибку, если запрошенный фрагмент находится вне границ файла.

 

[**Идвритефонтфилестреам**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) может получать содержимое файла шрифта из любого места, например с локального жесткого диска или из внедренных ресурсов.

 

 