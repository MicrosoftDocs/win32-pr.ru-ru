---
title: Settings. Balance
description: Свойство Balance указывает или получает текущее стерео сальдо.
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- Параметры. балансировка Windows Media Player
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
ms.openlocfilehash: 248cd3b2bbf735ef54382fb5b1be52755cad3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647991"
---
# <a name="settingsbalance"></a>Settings. Balance

Свойство **Balance** указывает или получает текущее стерео сальдо.

## <a name="syntax"></a>Синтаксис

проигрыватель. Settings. Balance

## <a name="possible-values"></a>Возможные значения

Это свойство имеет **номер** для чтения и записи (**Long**). Диапазон значений — от 100 до 100. значение по умолчанию равно нулю.

## <a name="remarks"></a>Комментарии

Нулевое значение указывает на то, что звук воспроизводится на равном томе как в левом, так и в правой канале. Значение 100 указывает, что звук воспроизводится только в левом канале. Значение 100 указывает, что звук воспроизводится только в правильном канале.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект параметров**](settings-object.md)
</dt> </dl>

 

 





