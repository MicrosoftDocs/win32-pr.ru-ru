---
title: Регистрация обратного вызова в Visual Basic
description: добавление обратного вызова в Visual Basic отличается от метода, используемого в VBScript.
ms.assetid: 6aebb855-cf5b-4134-b7f6-3a8b404b7ae8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7145a6c6ef80ede3ea2fdb1fd62a2661142fb6f0a85454389fe1c09c117e5b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126227"
---
# <a name="registering-a-callback-in-visual-basic"></a>Регистрация обратного вызова в Visual Basic

добавление обратного вызова в Visual Basic отличается от метода, используемого в VBScript. Функция **GetRef** , используемая в VBScript, отличается от используемой в Visual Basic. Поэтому разработчик должен создать объект [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , имеющий функцию обратного вызова в качестве метода по умолчанию. в этом разделе содержатся сведения, необходимые для разработки Visual Basic приложений.

**Реализация этого обратного вызова в приложении**

1.  Добавьте ссылки на две библиотеки объектов: Тлбтипес. olb и VboostTypes6. olb. Эти библиотеки объектов предоставляются с примером кода контрольной точки.
2.  Добавьте ссылку на Кбклиб. tlb. Этот файл определяет структуру функции обратного вызова.

    Кбклиб. tlb создается с помощью файла кбклиб. idl, который входит в состав примера кода контрольной точки. Рекомендуется, чтобы имя этого файла было изменено для функций обратного вызова, которые отличаются структурой их параметров. В этом примере для создания файла библиотеки типов используется MIDL.

3.  Напишите функцию обратного вызова. Параметры совпадают с параметрами в примере VBScript при [регистрации обратного вызова](registering-a-callback.md). Этот пример выводит строку при каждом поступлении события.
    ```VB
    Function eventHandler(ByVal callbackType As Variant, _
    ByVal svcObj As Variant, ByVal varName As Variant, _
    ByVal value As Variant) As Long

        On Error GoTo Error
        'Write some interesting code to do actual work here

        MsgBox "Event Handler Called"
        Exit Function

    Error:
        With Err
            If .Number > 0 Then
                eventHandler = .Number Or &H800A0000
            Else
                eventHandler = .Number
            End If
        End With
    End Function
    ```

    

4.  Добавьте функцию обратного вызова в объект [**иупнпсервице**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) , как показано в следующем примере, или в другой объект, например [**иупнпдевицефиндер**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder), используя соответствующую библиотеку типов обратного вызова (кбклиб. tbl).
    ```VB
    Public Sub AddCbFunction(upnpSvc As UPnPService)

        Dim X As CallbackIUnknownLib.CallBackInterface
        Dim obj As Object
        Dim ptinfo As ITypeInfo
        Dim ptcomp As ITypeComp

        With LoadTypeLibEx(App.Path & "\cbklib.tlb", _
          REGKIND_NONE).GetTypeComp
            .BindType "CallBackInterface", 0, ptinfo, ptcomp
        End With

        'NewDelegator is defined in FunctionDelegator.bas
        Set X = NewDelegator(AddressOf eventHandler) 
        Set obj = CreateStdDispatch(Nothing, ObjPtr(X), ptinfo)
        upnpSvc.AddCallback obj
    End Sub
    ```

    

В следующем примере объект [**иупнпсервице**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) передается в функцию. Затем функция обратного вызова добавляется в качестве параметра.


```VB
    Dim device as UPnPDevice
    Dim svcObj as UpnPService

    ' Initialize the device using the FindByType or using other methods of finding the devices
    Set svcObj = device.Services("appropriateService")
    Call AddCbFunction(svcObj)
```



## <a name="object-libraries-used-in-the-sample-code"></a>Библиотеки объектов, используемые в образце кода

В предыдущих примерах кода и образце контрольной точки используются некоторые из следующих библиотек объектов:

1.  Тлбтипес. olb — эта библиотека определяет некоторые типы типов и интерфейсы библиотеки типов, используемые в образце кода. он определяет некоторые функции, которые будут использоваться в Visual Basic, например [**лоадтипелибекс**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), которые уже доступны в C или C++.
2.  VboostTypes6. olb — эта библиотека определяет некоторые базовые типы, которые используются в Тлбтипес. olb и Функтионделегатор. BAS. дополнительные сведения о тлбтипес можно найти в книге *Advanced Visual Basic 6: энергопотребление для повседневных программ*, мэтью курланд (Addison-Wesley, июль 2000, ISBN: 0-201-70712-8). (Эта книга может быть недоступна в некоторых языках и странах.)

Пример кода контрольной точки и следующие библиотеки связаны с этим разделом и необходимы для реализации этого обратного вызова. Их можно найти с помощью примера кода контрольной точки:

-   Кбклиб. idl
-   Кбклиб. tlb
-   VboostTypes6. OLB
-   Тлбтипес. OLB
-   Функтионделегатор. BAS

 

 