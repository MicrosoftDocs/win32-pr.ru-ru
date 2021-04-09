---
description: Пример Еврпресентер
ms.assetid: 791a9816-4c40-4683-8b32-22f73d7fe84d
title: Пример Еврпресентер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde85de152c41f348b1aae74a8c0d67ca746cab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143111"
---
# <a name="evrpresenter-sample"></a>Пример Еврпресентер

Показывает, как реализовать пользовательский объект Presenter для [расширенного модуля подготовки видео](enhanced-video-renderer.md) (Евр). Пользовательский Presenter можно использовать с фильтром DirectShow Евр или с приемником Microsoft Media Foundation Евр.

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

Чтобы использовать этот пример в DirectShow, сделайте следующее:

1.  Выполните сборку примера.
2.  Зарегистрируйте EvrPresenter.dll.
3.  Выполните сборку и запустите пример Еврплайер. Этот пример включен в примеры DirectShow в Windows SDK.
4.  В меню **файл** выберите **Евр Presenter**.
5.  Выберите файл для воспроизведения.

## <a name="requirements"></a>Требования



| Продукт                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Загрузка образца

Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Улучшенный модуль подготовки видео](enhanced-video-renderer.md)
</dt> <dt>

[Написание выступающего Евр](how-to-write-an-evr-presenter.md)
</dt> <dt>

[Примеры пакетов SDK Media Foundation](media-foundation-sdk-samples.md)
</dt> </dl>

 

 
