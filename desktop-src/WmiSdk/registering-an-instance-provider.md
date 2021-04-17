---
description: Чтобы создать поставщик экземпляров WMI, необходимо зарегистрировать \_ \_ экземпляр Win32Provider, представляющий поставщика, с помощью экземпляра \_ \_ инстанцепровидеррегистратион.
ms.assetid: 5ac8e964-606f-4010-84a8-7c0ae6ca2133
ms.tgt_platform: multiple
title: Регистрация поставщика экземпляра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde8189559b04f2e45ac8357ab47cc17bd253fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544695"
---
# <a name="registering-an-instance-provider"></a>Регистрация поставщика экземпляра

Чтобы создать [*поставщик экземпляров*](gloss-i.md) WMI, необходимо зарегистрировать экземпляр [**\_ \_ Win32Provider**](--win32provider.md) , представляющий поставщика, с помощью экземпляра [**\_ \_ инстанцепровидеррегистратион**](--instanceproviderregistration.md). В качестве COM-объекта поставщик должен зарегистрироваться в операционной системе и инструментарии WMI. В следующей процедуре предполагается, что вы уже реализовали процесс регистрации, как описано в статье [Регистрация поставщика](registering-a-provider.md).

В следующей процедуре описывается регистрация поставщика экземпляра.

**Регистрация поставщика экземпляров**

1.  Создайте экземпляр класса [**\_ \_ Win32Provider**](--win32provider.md) , который описывает поставщик.
2.  Создайте экземпляр класса [**\_ \_ инстанцепровидеррегистратион**](--instanceproviderregistration.md) , описывающий набор функций поставщика.

    Класс [**\_ \_ инстанцепровидеррегистратион**](--instanceproviderregistration.md) наследует многие свойства от родительского класса [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md) , который предоставляет логические значения, которые указывают на поддержку определенных функций, и массив строк для указания поддержки запросов.

    Не забудьте пометить класс как как [**динамический**](standard-wmi-qualifiers.md) , так и квалификатор [**поставщика**](/windows/desktop/api/Provider/nl-provider-provider) . Квалификатор сигнализирует, что WMI должен использовать **динамический** поставщик для получения экземпляров класса. Квалификатор **поставщика** указывает имя поставщика, который должен использовать WMI.

В следующем примере кода показано, как зарегистрировать экземпляр [**\_ \_ Win32Provider**](--win32provider.md) и [**\_ \_ инстанцепровидеррегистратион**](--instanceproviderregistration.md) .

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
    QuerySupportLevels = { "WQL:UnarySelect" };
};
```

 

 



