---
description: Пример Еврпресентер
ms.assetid: 791a9816-4c40-4683-8b32-22f73d7fe84d
title: Пример Еврпресентер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe874483313d96f2ee6d9481fca7695d3ecfdba492f3e976f9f6c107c6114b1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118063658"
---
# <a name="evrpresenter-sample"></a>Пример Еврпресентер

Показывает, как реализовать пользовательский объект Presenter для [расширенного модуля подготовки видео](enhanced-video-renderer.md) (Евр). пользовательский presenter можно использовать с фильтром DirectShow евр или Microsoft Media Foundation приемником евр.

## <a name="apis-demonstrated"></a>Продемонстрированные API

В этом образце демонстрируются следующие интерфейсы Media Foundation:

-   [**имфклоккстатесинк**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**имфратесуппорт**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**имфтопологисервицелукупклиент**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient)
-   [**имфвидеодевицеид**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)
-   [**имфвидеодисплайконтрол**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)
-   [**имфвидеопресентер**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)

## <a name="usage"></a>Использование

В примере Еврпресентер создается библиотека DLL, которая является COM-сервером для выступающего. Перед использованием пользовательского Presenter необходимо зарегистрировать библиотеку DLL.

Чтобы использовать этот пример в Media Foundation:

1.  Выполните сборку примера.
2.  EvrPresenter.dll regsvr32.
3.  Выполните сборку и запустите [Пример мфплайер](/previous-versions//bb970516(v=vs.85)).
4.  В меню **файл** выберите **Открыть** файл.
5.  В диалоговом окне **Открытие файла** выберите **Custom Евр Presenter (пользовательский выступающий).**
6.  Выберите файл для воспроизведения.

Чтобы использовать этот пример в DirectShow:

1.  Выполните сборку примера.
2.  Зарегистрируйте EvrPresenter.dll.
3.  Выполните сборку и запустите пример Еврплайер. этот пример включен в примеры DirectShow в Windows SDK.
4.  В меню **файл** выберите **Евр Presenter**.
5.  Выберите файл для воспроизведения.

## <a name="requirements"></a>Требования



| Продукт                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Загрузка образца

этот пример доступен в [репозитории github для классических примеров Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Улучшенный модуль подготовки видео](enhanced-video-renderer.md)
</dt> <dt>

[Написание выступающего Евр](how-to-write-an-evr-presenter.md)
</dt> <dt>

[Примеры пакетов SDK Media Foundation](media-foundation-sdk-samples.md)
</dt> </dl>

 

 
