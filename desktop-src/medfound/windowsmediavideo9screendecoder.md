---
description: экранный декодер Windows media video 9 декодирует потоки, закодированные с помощью экранного кодировщика Windows Media видео 9.
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: Windows Экранный декодер видео 9 (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c2e081423c4c5efc2d44fdf78c7c6a94a00dae86d40d761a06ab0de07fa5d1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462394"
---
# <a name="windows-media-video-9-screen-decoder"></a>Windows Экранный декодер видео 9

экранный декодер Windows media video 9 декодирует потоки, закодированные с помощью [**экранного кодировщика Windows Media видео 9**](windowsmediavideo9screenencoder.md).

## <a name="class-identifier"></a>Идентификатор класса

идентификатор класса (CLSID) для декодера экрана Windows Media Video 9 представлен константой **CLSID \_ кмсскдекмедиаобжект**. Можно создать экземпляр декодера, вызвав **CoCreateInstance**.

## <a name="input-types"></a>Типы входных данных

код из четырех символов (FOURCC) для содержимого в формате Windows Media Video экрана версии 9 — "MSS2".

Декодер экрана версии 9 поддерживает следующие типы входных данных.

-   МЕДИАСУБТИПЕ \_ MSS2

## <a name="output-types"></a>Типы вывода

Декодеры экрана версии 9 поддерживают следующие типы выходных данных, если они используются в качестве объекта мультимедиа DirectX (DMO).

-   МЕДИАСУБТИПЕ \_ Rgb24
-   МЕДИАСУБТИПЕ \_ RGB32
-   МЕДИАСУБТИПЕ \_ ARGB32
-   МЕДИАСУБТИПЕ \_ RGB565
-   МЕДИАСУБТИПЕ \_ RGB555
-   МЕДИАСУБТИПЕ \_ RGB8

Декодеры экрана версии 9 поддерживают следующие типы выходных данных, если они используются в качестве Media Foundation преобразования (MFT).

-   Мфвидеоформат \_ Rgb24
-   Мфвидеоформат \_ RGB32
-   Мфвидеоформат \_ ARGB32
-   Мфвидеоформат \_ RGB565
-   Мфвидеоформат \_ RGB555
-   Мфвидеоформат \_ RGB8

## <a name="remarks"></a>Remarks

объект декодера экрана предоставляет интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) , чтобы объект можно было использовать в качестве объекта мультимедиа DirectX (DMO), и он предоставляет интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) , чтобы объект можно было использовать как преобразование Media Foundation (MFT).

декодер экрана ведет себя как DMO или MFT в зависимости от того, какие интерфейсы вы получаете и какая версия Windows выполняется. в следующей таблице показаны условия, при которых декодер экрана ведет себя в виде DMO или MFT.



| Операционная система            | Поведение декодера                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | декодер экрана Windows Media всегда ведет себя как DMO.                                                                                                                 |
| Windows Vista и Windows 7 | по умолчанию декодер экрана Windows мультимедиа ведет себя как DMO. При получении интерфейса [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) на экране декодера он ведет себя как MFT. |



 

Вы можете использовать один CLSID (CLSID \_ кмсскдекмедиаобжект) для создания декодера экрана версии 7 и декодера экрана версии 9. значение FOURCC для Windows Media Video экрана с кодировкой 7 — "MSS1". Декодер экрана версии 7 поддерживает \_ входной тип медиасубтипе MSS1.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Клиент<br/> | Windows XP, Windows Vista или Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Вмкодекдсп. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvsdecd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты кодека](codecobjects.md)
</dt> <dt>

[Реализация кодека](codecimplementation.md)
</dt> <dt>

[экранный кодек Windows Media видео 9](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Windows Кодировщик экрана видео в Media 9](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
