---
description: 'интерфейс иресизе должен поддерживаться любым настраиваемым фильтром изменения размеров видео для служб DirectShow editing Services (DES). Чтобы задать настраиваемый фильтр изменения размера, вызовите метод IRenderEngine2:: Сетресизергуид в подсистеме визуализации.'
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: Интерфейс Иресизе (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 19aabd7c04cb5350ef3da87e1a20db6b75f6546f0fbcf5af3422c152bcafcf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818073"
---
# <a name="iresize-interface"></a>Интерфейс Иресизе

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`IResize`интерфейс должен поддерживаться любым настраиваемым фильтром изменения размеров видео для служб DirectShow editing Services (DES). Чтобы задать настраиваемый фильтр изменения размера, вызовите метод [**IRenderEngine2:: сетресизергуид**](irenderengine2-setresizerguid.md) в подсистеме визуализации.

## <a name="members"></a>Элементы

Интерфейс **иресизе** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Иресизе** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иресизе** содержит следующие методы.



| Метод                                          | Описание                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [**получить \_ инпутсизе**](iresize-get-inputsize.md) | Возвращает текущий размер входных данных фильтра изменения размера.<br/>  |
| [**получить \_ mediaType**](iresize-get-mediatype.md) | Возвращает тип выходного носителя фильтра изменения.<br/>   |
| [**получить \_ Размер**](iresize-get-size.md)           | Возвращает текущий размер выходных данных и режим Stretch.<br/> |
| [**разместить \_ mediaType**](iresize-put-mediatype.md) | Задает тип выходного носителя.<br/>                       |
| [**\_размер размещения**](iresize-put-size.md)           | Задает размер выходных данных и режим Stretch.<br/>            |



 

## <a name="remarks"></a>Remarks

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | DirectX 9,0 или более поздней версии<br/>                                                         |
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Предоставление пользовательского изменения размера видео](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
