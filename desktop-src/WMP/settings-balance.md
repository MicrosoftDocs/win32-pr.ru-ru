---
title: Параметры. balance
description: Свойство Balance указывает или получает текущее стерео сальдо.
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- Параметры. балансировка проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Settings.balance
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e569c40214655fc643762da8580bd8d6a16e098b99c649bb27e1a1485d498931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569579"
---
# <a name="settingsbalance"></a>Параметры. balance

Свойство **Balance** указывает или получает текущее стерео сальдо.

## <a name="syntax"></a>Синтаксис

проигрыватель. Settings. Balance

## <a name="possible-values"></a>Возможные значения

Это свойство имеет **номер** для чтения и записи (**Long**). Диапазон значений — от 100 до 100. значение по умолчанию равно нулю.

## <a name="remarks"></a>Remarks

Нулевое значение указывает на то, что звук воспроизводится на равном томе как в левом, так и в правой канале. Значение 100 указывает, что звук воспроизводится только в левом канале. Значение 100 указывает, что звук воспроизводится только в правильном канале.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Параметры Объектами**](settings-object.md)
</dt> </dl>

 

 





