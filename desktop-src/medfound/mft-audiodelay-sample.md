---
description: '\_Пример АУДИОДЕЛАЙ MFT'
ms.assetid: 08f119f9-cacd-4000-96b6-60c8c0055e9c
title: Пример MFT_AudioDelay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4af3d89c7dda4a67a2fece09ff9e6d3bc0a63927e94b259df40334fd9ba29b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012674"
---
# <a name="mft_audiodelay-sample"></a>\_Пример АУДИОДЕЛАЙ MFT

Показывает, как реализовать звуковой эффекты в виде Media Foundation преобразования (MFT). Задержка аудио MFT принимает звук PCM в качестве входных данных, применяет результат задержки (echo) и выводит измененные аудиоданные.

## <a name="apis-demonstrated"></a>Продемонстрированные API

В этом образце демонстрируются следующие интерфейсы Microsoft Media Foundation:

-   [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>Использование

В \_ образце MFT аудиоделай создается библиотека DLL, которая является сервером COM для MFT. Перед использованием MFT необходимо зарегистрировать библиотеку DLL. С помощью средства Топоедит можно создать топологию, включающую в себя временную запись MFT. Дополнительные сведения о Топоедит см. в разделе [топоедит](topoedit.md). Можно также изменить [образец плайбаккфкс](/previous-versions//bb970336(v=vs.85)) для использования MFT. Вам потребуется изменить функцию Аддбранчтопартиалтопологи в проигрывателе Player. cpp. Измените следующую строку с:

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, GUID_NULL);
}
```

на:

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, CLSID_DelayMFT);
}
```

Значение CLSID \_ делаймфт объявляется в файле заголовка аудиоделайууидс. h в \_ папке образца MFT аудиоделай.

## <a name="requirements"></a>Требования



| Продукт                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Загрузка образца

этот пример доступен в [репозитории github для классических примеров Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Примеры пакетов SDK Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Преобразования Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[\_Пример использования градаций серого в MFT](mft-grayscale-sample.md)
</dt> <dt>

[Запись пользовательского MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 
