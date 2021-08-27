---
title: Функции-оболочки подключаемых модулей
description: Функции-оболочки, позволяющие вызывать открытую функцию для любого адаптера, подключенного к конвейеру, без необходимости вручную получать указатель на адаптер.
ms.assetid: a87536bf-3a10-4062-a509-db7f03172307
keywords:
- Windows api биометрическая платформа Windows api биометрической платформы, функции-оболочки подключаемых модулей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b3f6991d0723f284bb95ecfd40d7931c48aa8647fb52e2b34a959791a7338b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101254"
---
# <a name="plug-in-wrapper-functions"></a>Функции-оболочки подключаемых модулей

биометрическая платформа Windows API включает функции-оболочки, которые позволяют вызывать открытую функцию на любом адаптере, подключенном к конвейеру, без необходимости вручную получать указатель на адаптер. Каждая оболочка проверяет входные аргументы, получает указатель адаптера и вызывает запрошенную функцию. Например, оболочка **вбиоенгинесесашалгорисм** имеет следующую сигнатуру.


```C++
inline HRESULT
WbioEngineSetHashAlgorithm(
    __inout PWINBIO_PIPELINE Pipeline,
    __in SIZE_T AlgorithmBufferSize,
    __in PUCHAR AlgorithmBuffer
    )
{
    if (ARGUMENT_PRESENT(Pipeline) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface->SetHashAlgorithm))
    {
        return Pipeline->EngineInterface->SetHashAlgorithm(
                                            Pipeline,
                                            AlgorithmBufferSize,
                                            AlgorithmBuffer
                                            );
    }
    else
    {
        return E_NOTIMPL;
    }
}
```



Функция проверяет, что аргумент *конвейера* не равен **null**, существует адаптер ядра и существует функция [**енгинеадаптерсесашалгорисм**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) . Все функции-оболочки определены в \_ файле заголовка адаптера винбио. h. В следующих разделах рассматриваются доступные оболочки.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                               | Описание                                                                                                                        |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Оболочки адаптера подсистемы](engine-adapter-wrappers.md)<br/>   | Функции, которые можно использовать для вызова функций в адаптере подсистемы. Эти функции определены в Винбио \_ Adapter. h.<br/>  |
| [Оболочки адаптера датчика](sensor-adapter-wrappers.md)<br/>   | Функции, которые можно использовать для вызова функций в адаптере датчика. Эти функции определены в Винбио \_ Adapter. h.<br/>  |
| [служба хранилища Оболочки адаптеров](storage-adapter-wrappers.md)<br/> | Функции, которые можно использовать для вызова функций в адаптере хранилища. Эти функции определены в Винбио \_ Adapter. h.<br/> |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по подключаемым модулям](plug-in-reference.md)
</dt> </dl>

 

 





