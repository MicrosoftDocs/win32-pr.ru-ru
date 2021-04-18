---
description: Интерфейс IRenderEngine2 позволяет приложению заменить применяемый по умолчанию фильтр изменения размера видео, используемый службами редактирования DirectShow (DES). Базовый механизм визуализации и модуль интеллектуального просмотра поддерживают этот интерфейс.
ms.assetid: 37603c73-e199-431a-9a1e-a40c77755c70
title: Интерфейс IRenderEngine2 (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ed7802cf3d47d745b4e4733bb1fb60c61130b44a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679841"
---
# <a name="irenderengine2-interface"></a>Интерфейс IRenderEngine2

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`IRenderEngine2`Интерфейс позволяет приложению заменить применяемый по умолчанию фильтр изменения размера видео, используемый службами редактирования DirectShow (DES). [Базовый механизм визуализации](basic-render-engine.md) и [модуль интеллектуального просмотра](smart-render-engine.md) поддерживают этот интерфейс.

## <a name="members"></a>Элементы

Интерфейс **IRenderEngine2** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IRenderEngine2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IRenderEngine2** содержит следующие методы.



| Метод                                                  | Описание                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**сетресизергуид**](irenderengine2-setresizerguid.md) | Указывает идентификатор CLSID пользовательского фильтра изменения размера, предоставленного приложением.<br/> |



 

## <a name="remarks"></a>Комментарии

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

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

 

 
