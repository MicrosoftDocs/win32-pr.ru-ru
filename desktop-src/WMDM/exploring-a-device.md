---
title: Изучение устройства
description: Изучение устройства
ms.assetid: 8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0
keywords:
- Диспетчер устройств Windows Media, изучение устройств
- Диспетчер устройств, изучение устройств
- Программное руководством, изучение устройств
- Классические приложения, изучение устройств
- Создание приложений диспетчер устройств Windows Media, изучение устройств
- изучение устройств
- хранилищах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc154960a4c95efbdf2626271ba90000df99ae8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410989"
---
# <a name="exploring-a-device"></a>Изучение устройства

Изучение устройства похоже на изучение диска. Все объекты на устройстве называются *хранилищами*. Хранилищем может быть файл, папка или абстрактный объект (например, список воспроизведения) на устройстве. Необходимо изучить атрибуты и метаданные хранилища (если они поддерживаются), чтобы понять, какой тип хранилища он имеет. Хранилища организованы иерархически на устройстве; Каждое хранилище имеет ровно один родительский объект, и все хранилища в конечном итоге попадут в одно хранилище корневых устройств, обычно именуемое " \\ ".

Следующие шаги описывают изучение устройства:

1.  Получите интерфейс [**ивмдмдевице**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) устройства, как описано в разделе [Перечисление устройств](enumerating-devices.md).
2.  Вызовите метод [**ивмдмдевице:: енумстораже**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) , чтобы получить интерфейс [**ивмдменумстораже**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) . Этот интерфейс используется для получения всех дочерних объектов хранилища, возвращающих этот интерфейс. При получении этого интерфейса с устройства, как мы здесь, он будет хранить только одно хранилище: хранилище корневого устройства.
3.  Вызовите метод [**ивмдменумстораже:: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) со значением счетчика 1, чтобы получить интерфейс [**ивмдмстораже**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) для хранилища корневого устройства. (На устройстве нельзя запрашивать более одного дочернего элемента.)
4.  Проверьте все хранилища на устройстве, рекурсивно вызвав [**ивмдмстораже:: енумстораже**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) , а затем **Ивмдменумстораже:: Next** , чтобы получить дочерние элементы хранилища. Чтобы узнать, есть ли у хранилища дочерние элементы, чтобы избежать вызовов **енумстораже** и **Next**, можно вызвать [**ивмдмстораже:: OutAttribute**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) , чтобы проверить наличие флагов вмдма \_ attr, \_ \_ имеющих файлы или вмдм в атрибуте \_ \_ Storage \_ attr \_ есть \_ папки. Дополнительные сведения о том, как получить свойства хранилища, см. в статьях [Получение и установка метаданных и атрибутов](getting-and-setting-metadata-and-attributes.md) , а также [Получение и установка метаданных и атрибутов в приложении](getting-and-setting-metadata-and-attributes-in-the-application.md).

Диспетчер устройств Windows Media не предоставляет стандартный набор папок для хранения мультимедиа определенного типа (например, папка "Мои списки воспроизведения" для списков воспроизведения). Каждое устройство имеет уникальную файловую систему, и вам придется выбрать подходящее место для поиска или отправки определенного файла.

> [!Note]  
> Проводник Windows может отображать виртуальные папки, которые на самом деле не существуют на устройстве. Например, виртуальные папки — это папки "Media" и "Data", отображаемые для устройств MTP. Эти папки создаются Windows, чтобы упростить загрузку для конечных пользователей. они на самом деле не существуют на устройстве. Приложение не должно зависеть от поиска этих типов общих папок. И наоборот, проводник Windows может не показывать некоторые папки или объекты, существующие на устройстве (например, списки воспроизведения).

 

В следующем примере кода C++ показано рекурсивное исследование устройства. В нем используются две функции:

-   Експлоредевице — начальная функция, которая получает указатель устройства и получает указатель на корневой перечислитель для этого устройства.
-   Рекурсивиксплорестораже, который вызывается для рекурсивного изучения устройства.


```C++
// Get the root enumerator and start the recursive function.
HRESULT ExploreDevice(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get a root enumerator.
    CComPtr<IWMDMEnumStorage> pEnumStorage;
    hr = pDevice->EnumStorage(&pEnumStorage);
    if (SUCCEEDED(hr))
    {
        RecursiveExploreStorage(pEnumStorage);
    }
    return hr;
}

// Recursively explore a storage.
void RecursiveExploreStorage(IWMDMEnumStorage* pEnumStorage)
{
    HRESULT hr = S_OK;
    CComPtr<IWMDMStorage> pStorage;

    ULONG numRetrieved = 0;
    // Loop through all storages in the current storage.
    while((pEnumStorage->Next(1, &pStorage, &numRetrieved) == S_OK) && (numRetrieved == 1))
    {
        // Get the name of the object.
        const UINT MAX_LEN = 255;
        WCHAR name[MAX_LEN];
        hr = pStorage->GetName((LPWSTR)&name, MAX_LEN);
        // TODO: Display the retrieved storage name

        // If this is a folder, recurse into it.
        if (attributes & WMDM_FILE_ATTR_FOLDER)
        {
            CComPtr<IWMDMEnumStorage> pEnumSubStorage;
            hr = pStorage->EnumStorage(&pEnumSubStorage);
            if (SUCCEEDED(hr)
            {
                RecursiveExploreStorage(pEnumSubStorage);
            }
        }
        pStorage.Release();
    } // Get the next storage pointer.
    return;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Создание приложения диспетчер устройств Windows Media**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




