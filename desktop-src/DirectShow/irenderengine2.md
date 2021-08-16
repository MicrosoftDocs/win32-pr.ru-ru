---
description: интерфейс IRenderEngine2 позволяет приложению заменить применяемый по умолчанию фильтр изменения размера видео, используемый службами DirectShow editing Services (DES). Базовый механизм визуализации и модуль интеллектуального просмотра поддерживают этот интерфейс.
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
ms.openlocfilehash: 39f1bc68fc6cd76e87d1998047cb211b3a8aa8e263c90e0494c7eaf15d52f75f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818512"
---
# <a name="irenderengine2-interface"></a>Интерфейс IRenderEngine2

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`IRenderEngine2`интерфейс позволяет приложению заменить применяемый по умолчанию фильтр изменения размера видео, используемый службами DirectShow editing Services (DES). [Базовый механизм визуализации](basic-render-engine.md) и [модуль интеллектуального просмотра](smart-render-engine.md) поддерживают этот интерфейс.

## <a name="members"></a>Элементы

Интерфейс **IRenderEngine2** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IRenderEngine2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IRenderEngine2** содержит следующие методы.



| Метод                                                  | Описание                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**сетресизергуид**](irenderengine2-setresizerguid.md) | Указывает идентификатор CLSID пользовательского фильтра изменения размера, предоставленного приложением.<br/> |



 

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

 

 
