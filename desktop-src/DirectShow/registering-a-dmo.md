---
description: Регистрация DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: Регистрация DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5635f7b05edb13da80adb62104db5c412fa55608ec2f9b5214380b7d9a095e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904544"
---
# <a name="registering-a-dmo"></a>Регистрация DMO

чтобы клиенты могли использовать DMO, идентификатор CLSID должен быть зарегистрирован в системе пользователя. Это делается с помощью функции **DllRegisterServer** библиотеки DLL. Если используется библиотека активных шаблонов (ATL), мастер ATL автоматически создает эту функцию.

вы также можете зарегистрировать DMO в одной или нескольких категориях стандартных DMO. это позволяет клиентам обнаруживать DMO с помощью функции [**дмоенум**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) . категории определяются по идентификатору guid и перечислены в разделе [DMO guids](dmo-guids.md).

регистрация DMO в категории является необязательной. для этого вызовите функцию [**дморегистер**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) и укажите понятное имя DMO, CLSID и категорию. При необходимости можно также зарегистрировать набор типов мультимедиа, поддерживаемых дмос. дополнительные сведения см. в разделе [DMO Media types](dmo-media-types.md).

в следующем примере показано, как зарегистрировать звуковое действие DMO, поддерживающее входные и выходные данные PCM. В этом случае типы входных и выходных данных одинаковы.


```C++
STDAPI DllRegisterServer(void)
{
    // Register the DMO as a PCM audio effect DMO
    DMO_PARTIAL_MEDIATYPE mt;
    mt.type    = MEDIATYPE_Audio;
    mt.subtype = MEDIASUBTYPE_PCM;
    HRESULT hr = DMORegister(
        L"MyDMO",                  // Friendly name
        CLSID_MyDMO,               // CLSID
        DMOCATEGORY_AUDIO_EFFECT,  // Category
        0,                         // Flags 
        1,                         // Number of input types
        &mt,                       // Array of input types
        1,                         // Number of output types
        &mt);                      // Array of output types

    if (FAILED(hr)) return hr;

    // Registers the object, with no typelib.
    return _Module.RegisterServer(FALSE);
}
```



В этом примере предполагается, что для создания проекта использовалась библиотека ATL. Последняя строка функции вызывает стандартный метод ATL для регистрации сервера COM. Если вы не используете ATL, функция будет выглядеть иначе.

**Отмена регистрации DMO**

Функция **DllUnregisterServer** должна удалить все записи реестра, создаваемые функцией **DllRegisterServer** . при вызове **дморегистер** при регистрации DMO необходимо [**дмаунрегистер**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) с той же категорией при отмене регистрации DMO.

В следующем примере удаляются записи реестра, созданные в предыдущем примере.


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



**DirectShow Неуспешные значения**

для создания графов фильтров DirectShow присваивает дмос значение по умолчанию. это значение можно переопределить, добавив запись реестра в раздел реестра DMO в \_ \_ корневой CLSID классов HKEY \\ . Включите значение **DWORD** с именем `Merit` , значение которого указывает на неуспешный выбор.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Запись DMO](writing-a-dmo.md)
</dt> </dl>

 

 



