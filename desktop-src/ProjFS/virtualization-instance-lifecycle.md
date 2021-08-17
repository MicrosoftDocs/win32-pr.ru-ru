---
title: Жизненный цикл экземпляра виртуализации
description: Общие сведения о жизненном цикле экземпляра Прожфс Virtualization.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: bbaaf5eca5481f3959e3e5afeb36a8cf6b264c939e8eb2cc9d84ba501d3c8530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792388"
---
# <a name="virtualization-instance-lifecycle"></a>Жизненный цикл экземпляра виртуализации

Приложение поставщика поддерживает один или несколько экземпляров виртуализации.  Каждый экземпляр виртуализации проходит через четыре этапа в своем жизненном цикле:

1. Создание
2. Запуск
3. Параметры выполнения
4. Shutdown

Обратите внимание, что после завершения работы экземпляра виртуализации поставщику не нужно повторно создавать его для повторного использования.  Его можно просто запустить снова.

> **Примечание**. в этом разделе приведены примеры API-интерфейсов прожфс.  Каждый пример предназначен для демонстрации базового использования API.  Документацию по параметрам, не используемым в этих примерах, см. в [справочнике по API прожфс](/windows/desktop/api/_projfs).

## <a name="creating-a-virtualization-root"></a>Создание корня виртуализации

Прежде чем поставщик может запустить экземпляр виртуализации, который будет выполнять проецирование элементов в локальную файловую систему, необходимо создать корень виртуализации.  Корневой узел виртуализации — это каталог, в котором поставщик проецирует дерево каталогов и файлов.

Чтобы создать корень виртуализации, поставщик должен выполнить следующие действия:

1. Создайте каталог, который будет служить корнем виртуализации.

    Поставщик создает каталог, используемый в качестве корня виртуализации, с помощью, например **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:

    ```C++
    HRESULT hr;
    const wchar_t* rootName = LR"(C:\virtRoot)";
    if (!CreateDirectoryW(rootName, nullptr))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        wprintf(L"Failed to create virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

1. Создайте идентификатор экземпляра виртуализации.

    Каждый экземпляр виртуализации имеет уникальный идентификатор, именуемый _идентификатором экземпляра виртуализации_.  Система использует это значение для указания того, с каким экземпляром виртуализации связано его содержимое.

    ```C++
    GUID instanceId;
    hr = CoCreateGuid(&instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to create instance ID (0x%08x)\n", hr);
        return;
    }
    ```

1. Пометьте новый каталог как корень виртуализации.

    Поставщик вызывает **[пржмаркдиректорясплацехолдер](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** , чтобы пометить новый каталог как корень виртуализации и назначить его экземпляру виртуализации.

    ```C++
    hr = PrjMarkDirectoryAsPlaceholder(rootName,
                                       nullptr,
                                       nullptr,
                                       &instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to mark virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

Поставщику необходимо только один раз создать корень виртуализации для каждого экземпляра виртуализации.  После создания корня его связанный экземпляр может многократно запускаться и останавливаться без повторного создания корня.

## <a name="starting-a-virtualization-instance"></a>Запуск экземпляра виртуализации

После создания корня виртуализации поставщик должен запустить экземпляр виртуализации.  Это сигнализирует Прожфс, что поставщик готов получить обратные вызовы и предоставить данные.

Чтобы запустить экземпляр виртуализации, поставщик должен выполнить следующие действия:

1. Настройте таблицу обратного вызова.

    Прожфс взаимодействует с поставщиком, вызывая подпрограммы обратного вызова, реализованные поставщиком.  Поставщик заполняет [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) структуру указателями на подпрограммы обратного вызова.

    ```C++
    PRJ_CALLBACKS callbackTable;

    // Supply required callbacks.
    callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
    callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
    callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
    callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
    callbackTable.GetFileDataCallback = MyGetFileDataCallback;

    // The rest of the callbacks are optional.
    callbackTable.QueryFileNameCallback = nullptr;
    callbackTable.NotificationCallback = nullptr;
    callbackTable.CancelCommandCallback = nullptr;
    ```

1. Запустите экземпляр.

    Поставщик вызывает **[пржстартвиртуализинг](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** для запуска экземпляра виртуализации.

    ```C++
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
    hr = PrjStartVirtualizing(rootName,
                              &callbackTable,
                              nullptr,
                              nullptr,
                              &instanceHandle);
    if (FAILED(hr))
    {
        wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
        return;
    }
    ```
    Параметр _InstanceHandle_ **пржстартвиртуализинг** возвращает дескриптор экземпляра виртуализации.  Поставщик использует этот обработчик при вызове других интерфейсов API Прожфс.

## <a name="virtualization-instance-runtime"></a>Среда выполнения экземпляра виртуализации

После того как вызов **пржстартвиртуализинг** возвращает, прожфс будет вызывать подпрограммы обратного вызова поставщика в ответ на операции файловой системы в экземпляре виртуализации.  Сведения о том, как поставщик может управлять различными операциями файловой системы, см. в следующих разделах:

* [Перечисление файлов и каталогов](enumerating-files-and-directories.md)
* [Предоставление данных файлов](providing-file-data.md)
* [Уведомления операций файловой системы](file-system-operation-notifications.md)
* [Обработка изменений представления](handling-view-changes.md)

## <a name="shutting-down-a-virtualization-instance"></a>Завершение работы экземпляра виртуализации

Чтобы сообщить Прожфс о том, что поставщик желает приостанавливаться на получении обратных вызовов и предоставить данные, поставщик должен прерывать экземпляр виртуализации.  Для этого поставщик вызывает **[пржстопвиртуализинг](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, передавая ему обработчик на экземпляр виртуализации, полученный из вызова **пржстартвиртуализинг**.

```C++
PrjStopVirtualizing(instanceHandle);
```

Обратите внимание, что до возвращения этого вызова Прожфс может продолжать вызывать подпрограммы обратного вызова поставщика.