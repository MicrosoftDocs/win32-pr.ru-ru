---
title: External. Виевпараметерс
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | External. Виевпараметерс
ms.assetid: 0afabe35-2857-413a-a662-1a76d3fb75fe
keywords:
- Внешний Виевпараметерс проигрыватель Windows Media
topic_type:
- apiref
api_name:
- External.viewParameters
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0adec580a68bd3f6b92beef1de814729848179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695054"
---
# <a name="externalviewparameters"></a>External. Виевпараметерс

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Свойство **виевпараметерс** извлекает параметры, связанные с текущим представлением в проигрывателе Windows Media.

## <a name="syntax"></a>Синтаксис

**Window. external. Виевпараметерс**

## <a name="possible-values"></a>Возможные значения

Это свойство возвращает **строку**, доступную только для чтения.

## <a name="remarks"></a>Комментарии

Это свойство извлекает параметры, которые ранее были заданы в Интернет-магазине. Например, в Интернет-магазине можно указать параметры представления в параметре *виевпарамс* метода [Чанжевиев](external-changeview.md) или параметр *params* метода [чанжевиевонлинелист](external-changeviewonlinelist.md) .

Параметры представления не обрабатываются проигрывателем Windows Media. Они создаются Интернет-магазином и имеют значение только в Интернет-магазине.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Внешний объект для Интернет-магазинов типа 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





