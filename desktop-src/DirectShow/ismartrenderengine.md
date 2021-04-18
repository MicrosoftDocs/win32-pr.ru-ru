---
description: Интерфейс Исмартрендеренгине предоставляет методы, поддерживающие интеллектуальное повторное сжатие в службах редактирования DirectShow (DES). Модуль интеллектуального просмотра предоставляет этот интерфейс.
ms.assetid: 0e03708f-e471-4188-a212-ec5e951d20fa
title: Интерфейс Исмартрендеренгине (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e82ba73764adc27ff366533c3b5cfdc2eebc7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675378"
---
# <a name="ismartrenderengine-interface"></a>Интерфейс Исмартрендеренгине

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`ISmartRenderEngine`Интерфейс предоставляет методы, поддерживающие интеллектуальное повторное сжатие в [службах редактирования DirectShow](directshow-editing-services.md) (DES). Модуль интеллектуального просмотра предоставляет этот интерфейс.

## <a name="members"></a>Элементы

Интерфейс **исмартрендеренгине** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Исмартрендеренгине** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **исмартрендеренгине** содержит следующие методы.



| Метод                                                                | Описание                                                                          |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**жетграупкомпрессор**](ismartrenderengine-getgroupcompressor.md)   | Извлекает фильтр сжатия для указанной группы.<br/>                 |
| [**сетфиндкомпрессоркб**](ismartrenderengine-setfindcompressorcb.md) | Не реализован.<br/>                                                          |
| [**сетграупкомпрессор**](ismartrenderengine-setgroupcompressor.md)   | Задает фильтр сжатия, используемый при подготовке к просмотру указанной группы.<br/> |



 

## <a name="remarks"></a>Комментарии

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Подготовка проекта](rendering-a-project.md)
</dt> </dl>

 

 
