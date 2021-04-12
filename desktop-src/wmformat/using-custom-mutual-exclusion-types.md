---
title: Использование настраиваемых типов взаимного исключения
description: Использование настраиваемых типов взаимного исключения
ms.assetid: 9a4d760c-80af-4c67-823d-6da2732671ff
keywords:
- ивммутуалексклусион
- взаимное исключение, интерфейс Ивммутуалексклусион
- взаимное исключение, пользовательские типы
- профили, пользовательские типы взаимных исключений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051e95bfb3f5ef8e39af31368227cf4918b897d2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104133495"
---
# <a name="using-custom-mutual-exclusion-types"></a>Использование настраиваемых типов взаимного исключения

В профиле можно использовать взаимоисключающие объекты для удовлетворения потребностей пользовательских сценариев. Передавая значение GUID CLSID \_ вммутекс \_ Unknown в [**Ивммутуалексклусион:: сеттипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), вы сообщаете об объекте взаимного исключения, который используется в пользовательском сценарии.

Необходимо вручную управлять выбором потока при чтении файла с пользовательским взаимоисключающим значением. Объект модуля чтения будет использовать первый поток, добавляемый в взаимное исключение в качестве значения по умолчанию.

Чтобы создать настраиваемый объект взаимного исключения и добавить его в профиль, выполните следующие действия.

1.  Создайте диспетчер профилей, вызвав функцию [**вмкреатепрофилеманажер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
2.  Либо Начните с существующего профиля, либо создайте совершенно новый.
    -   Если вы используете существующий профиль, вызовите один из методов Load интерфейса [**ивмпрофилеманажер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) . Перейдите к шагу 4.
    -   Если создается совершенно новый профиль, вызовите метод [**ивмпрофилеманажер:: креатимптипрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).
3.  Добавьте потоки в новый профиль, вызвав [**ивмпрофиле:: креатеневстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream). При необходимости настройте потоки с помощью методов [**ивмстреамконфиг**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig). Можно также вызвать **QueryInterface** для доступа к другим интерфейсам в объекте конфигурации потока.

    **Креатеневстреам** создает только объект конфигурации потока и не влияет на профиль. После правильной настройки потока необходимо вызвать метод [**ивмпрофиле:: аддстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) , чтобы добавить поток в профиль.

4.  Создайте объект взаимного исключения, вызвав [**ивмпрофиле:: креатеневмутуалексклусион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).
5.  Добавьте нужные потоки в объект взаимного исключения, вызвав [**ивмстреамлист:: аддстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (доступен непосредственно из [**ивммутуалексклусион**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), который наследуется от [**ивмстреамлист**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).
6.  Задайте тип взаимного исключения для настраиваемого объекта, вызвав [**ивммутуалексклусион:: сеттипе**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype). Передайте CLSID \_ вммутекс \_ Unknown в качестве типа GUID.
7.  Добавьте настроенный объект взаимного исключения в профиль, вызвав [**ивмпрофиле:: аддмутуалексклусион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивммутуалексклусион**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**Интерфейс Ивмпрофиле**](iwmprofile.md)
</dt> <dt>

[**Интерфейс Ивмпрофилеманажер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Интерфейс Ивмстреамконфиг**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[**Интерфейс Ивмстреамлист**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)
</dt> <dt>

[**Использование взаимного исключения**](using-mutual-exclusion.md)
</dt> <dt>

[**вмкреатепрофилеманажер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
</dt> </dl>

 

 




