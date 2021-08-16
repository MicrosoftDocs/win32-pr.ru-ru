---
description: Определение поддерживаемых ставок
ms.assetid: 7f2b64e1-1062-4f77-b8e0-62b6d962ae8b
title: Определение поддерживаемых ставок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aadbf0f9a0ce9608b58019d64ddb18a2227bbeb2941540086a6f998e40ebc3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878946"
---
# <a name="how-to-determine-supported-rates"></a>Определение поддерживаемых ставок

Прежде чем изменять скорость воспроизведения, приложение должно проверить, поддерживается ли скорость воспроизведения объектами в конвейере. Интерфейс [**имфратесуппорт**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) предоставляет методы для получения максимальной скорости прямого и обратного тарифа, поддерживаемой частоты, ближайшей к запрошенной ставке, и самой медленной скорости. Каждый из этих запросов скорости может задавать направление воспроизведения и необходимость использования тонкого. Точный уровень воспроизведения запрашивается с помощью интерфейса [**имфратеконтрол**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) .

Сведения об изменении скорости воспроизведения см. в разделе [Установка скорости воспроизведения для сеанса мультимедиа](how-to-set-the-playback-rate-on-the-media-session.md).

Общие сведения о скорости воспроизведения см. в разделе [сведения об управлении скоростью](about-rate-control.md).

## <a name="to-determine-the-current-playback-rate"></a>Определение текущей скорости воспроизведения

1.  Получение службы управления скоростью из сеанса мультимедиа.

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    Передайте инициализированный указатель интерфейса [**имфмедиасессион**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) в параметре *объект punkObject* объекта [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

    Приложение должно запросить службу управления скоростью через сеанс мультимедиа. На внутреннем уровне сеанс мультимедиа запрашивает объекты в топологии.

2.  Вызовите метод [**имфратеконтрол:: Rate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) , чтобы получить текущую скорость воспроизведения.

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    Параметр *пфсин* параметра [**Rate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) получает **логическое** значение, указывающее, является ли поток в данный момент тонким. Приложение должно передать **значение NULL** , если не нужно запрашивать тонкую поддержку потока. Параметр *пфлрате* получает текущую скорость воспроизведения.

## <a name="to-determine-the-nearest-supported-rate"></a>Определение ближайшей поддерживаемой частоты

1.  Получите службу поддержки по скорости из сеанса мультимедиа.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Передайте инициализированный указатель интерфейса [**имфмедиасессион**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) в параметре *объект punkObject* объекта [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

2.  Вызовите метод [**имфратесуппорт:: исратесуппортед**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) , чтобы получить поддерживаемую частоту, ближайшую к запрошенному темпу воспроизведения.

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    В примере запрашивается, поддерживается ли скорость воспроизведения 4,0 с тонкой. Это указывается путем передачи значения **true** в параметре *ФСИН* объекта [**исратесуппортед**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported). Если эта скорость поддерживается, *актуалрате* содержит частоту воспроизведения 4,0, и вызов будет выполнен успешно с возвращаемым значением S \_ ОК. Если точный коэффициент воспроизведения не поддерживается, в *актуалрате* получается Ближайшая поддерживаемая ставка. Если скорость не поддерживается и нет доступной ближайшей скорости воспроизведения, вызов возвращает соответствующий код ошибки.

    Эти значения могут изменяться в зависимости от того, какие компоненты конвейера загружены. Поэтому при загрузке нового топололги необходимо повторно запрашивать значения.

    Если желаемая скорость воспроизведения не поддерживается, можно запросить каждый объект в топологии по отдельности, чтобы определить, не поддерживает ли конкретный компонент скорость. Вы можете перестроить топологию без этого компонента, а затем воспроизвести ее с желаемой скоростью. Например, если каждый компонент, за исключением модуля подготовки звука, поддерживает заданную скорость, можно перестроить топологию без звуковой ветви и воспроизвести желаемую скорость без звука.

## <a name="to-determine-the-slowest-supported-rate"></a>Определение самой медленной поддерживаемой скорости

1.  Получите службу поддержки по скорости из сеанса мультимедиа.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Передайте инициализированный указатель интерфейса [**имфмедиасессион**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) в параметре *объект punkObject* объекта [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

2.  Вызовите метод [**имфратесуппорт:: жетсловестрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) , чтобы получить наиболее медленную поддерживаемую частоту.

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    В примере запрашиваются самые медленные обратные скорости воспроизведения с тонкой. Нижняя граница получается в параметре *словестрате* объекта [**жетсловестрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).

    Если обратная или тонкое воспроизведение не поддерживается, вызов возвращает соответствующий код ошибки.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сеанс мультимедиа](media-session.md)
</dt> <dt>

[Управление скоростью](rate-control.md)
</dt> <dt>

[поиск, Быстрая прокрутка и обратная игра](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



