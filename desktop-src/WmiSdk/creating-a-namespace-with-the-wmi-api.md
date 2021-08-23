---
description: Другим способом создания пространства имен является использование API WMI для программного создания пространства имен.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Создание пространства имен с помощью API инструментария WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8192bb38b60c3d0ddefb8cc1e5cb7b5f78cb0f5ba7937d39784729e0f61f70b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612544"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a>Создание пространства имен с помощью API инструментария WMI

Другим способом создания пространства имен является использование API WMI для программного создания пространства имен. Преимущество создания пространства имен программным способом заключается в том, что пространство имен можно создать из приложения. Однако использование API инструментария WMI сложнее, чем использование кода MOF-файл (MOF), и вы не можете легко предоставлять общий доступ к пространствам имен другим разработчикам.

В следующей процедуре описывается создание пространства имен с помощью API инструментария WMI.

**Создание пространства имен с помощью API инструментария WMI**

1.  Используйте [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) для получения указателя на объект [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) , указывающий на класс системы [**\_ \_ пространства имен**](--namespace.md) .
2.  Определите экземпляр класса системы [**\_ \_ пространства имен**](--namespace.md) с помощью вызова [**ивбемклассобжект:: спавнинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).
3.  Задайте свойство **Name** экземпляра [**\_ \_ пространства имен**](--namespace.md) с помощью вызова [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).
4.  Создайте пространство имен с помощью вызова [**IWbemServices::P утинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).

    Параметр " *закрепление* " [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) должен указывать на новый экземпляр.

 

 



