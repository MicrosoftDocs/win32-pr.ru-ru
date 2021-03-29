---
title: Интерфейс IWMProfile
description: Интерфейс Ивмпрофиле является основным интерфейсом для объекта профиля.
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
keywords:
- Формат Windows Media в интерфейсе Ивмпрофиле
- Ивмпрофиле интерфейса Windows Media Format, описание
topic_type:
- apiref
api_name:
- IWMProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- wmsdkidl.h
ms.openlocfilehash: f814df820bd50a36abf2ee8e453549f46c9c5c9e
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "105661791"
---
# <a name="iwmprofile-interface"></a>Интерфейс IWMProfile

Интерфейс **ивмпрофиле** является основным интерфейсом для объекта [*профиля*](wmformat-glossary.md) . Объект профиля используется для настройки пользовательских профилей. **Ивмпрофиле** можно использовать для создания, удаления или изменения объектов конфигурации потока и взаимоисключающих объектов. Можно также задать и получить общие сведения о профиле. Чтобы получить доступ ко всем функциям объекта Profile, следует использовать [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3), который наследует от **ивмпрофиле** и [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2).

**Ивмпрофиле** также доступен через объект Reader, где его можно использовать для получения сведений о потоках файла, загружаемого в средство чтения. При доступе к **ивмпрофиле** из средства чтения можно вносить изменения в профиль, но ни один из изменений не может быть сохранен в файле. Часто бывает удобно использовать профиль существующего файла в качестве основы нового профиля. Синхронный модуль чтения поддерживает **ивмпрофиле** таким же образом, как и читатель.

Данные профиля, полученные с помощью средства чтения или синхронного модуля чтения, не поступают из пркс-файла. Средство чтения использует сведения в файле ASF для сборки конфигураций потоков. Поэтому некоторые сведения о профиле, такие как имя и описание, недоступны через средство чтения.

Существует несколько способов получить указатель на интерфейс **ивмпрофиле** . Диспетчер профилей имеет методы для создания нового профиля и доступа к существующим профилям. Все эти методы задают указатель **ивмпрофиле** . При чтении файла указатель на **ивмпрофиле** можно получить, вызвав метод **QueryInterface** любого интерфейса чтения. Аналогичным образом, любой интерфейс синхронного объекта Reader может получить указатель с вызовом **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3).

## <a name="members"></a>Элементы

Интерфейс **ивмпрофиле** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Ивмпрофиле** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ивмпрофиле** содержит следующие методы.



| Метод                                                                  | Описание                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**аддмутуалексклусион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)             | Добавляет объект взаимного исключения в профиль.<br/>                                   |
| [**аддстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream)                               | Добавляет поток в профиль.<br/>                                                    |
| [**креатеневмутуалексклусион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | Создает объект взаимного исключения для профиля.<br/>                               |
| [**креатеневстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)                   | Создает объект конфигурации потока для профиля.<br/>                           |
| [**GetDescription**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getdescription)                     | Извлекает описание профиля.<br/>                                        |
| [**жетмутуалексклусион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | Извлекает объект взаимного исключения из профиля.<br/>                            |
| [**жетмутуалексклусионкаунт**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount)   | Возвращает количество объектов взаимного исключения в профиле.<br/>                 |
| [**GetName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getname)                                   | Возвращает имя профиля.<br/>                                               |
| [**GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                               | Извлекает из профиля поток, используя номер индекса.<br/>                     |
| [**жетстреамбинумбер**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)               | Извлекает поток, используя номер потока из профиля.<br/>            |
| [**жетстреамкаунт**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)                     | Возвращает количество потоков в профиле.<br/>                                  |
| [**GetVersion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getversion)                             | Возвращает номер версии служб Microsoft Windows Media в профиле.<br/> |
| [**реконфигстреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)                     | Позволяет включить в профиль изменения, внесенные в конфигурацию потока.<br/>    |
| [**ремовемутуалексклусион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion)       | Удаляет объект взаимного исключения из профиля.<br/>                              |
| [**ремовестреам**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestream)                         | Удаляет поток из профиля.<br/>                                               |
| [**ремовестреамбинумбер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber)         | Удаляет поток из профиля.<br/>                                               |
| [**SetDescription**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setdescription)                     | Указывает описание профиля.<br/>                                        |
| [**SetName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setname)                                   | Задает имя профиля.<br/>                                               |



 

Сведения о том, какие интерфейсы можно получить с помощью метода QueryInterface этого интерфейса, см. в разделе, посвященном объекту, в котором реализован этот интерфейс.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейсы**](interfaces.md)
</dt> <dt>

[**Интерфейс Ивмпрофилеманажер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Объект диспетчера профилей**](profile-manager-object.md)
</dt> <dt>

[**Объект модуля чтения**](reader-object.md)
</dt> <dt>

[**Объект модуля синхронного чтения**](synchronous-reader-object.md)
</dt> <dt>

[**Работа с профилями**](working-with-profiles.md)
</dt> </dl>

 

