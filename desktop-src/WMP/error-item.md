---
title: Error. Item, метод
description: Метод Item извлекает объект Ерроритем из очереди ошибок.
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- метод Item проигрыватель Windows Media Player
- метод Item проигрыватель Windows Media, класс Error
- Класс ошибок Windows Media Player, метод Item
topic_type:
- apiref
api_name:
- Error.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5545df50fce05ff5a10a5f870d1ec07648434fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694512"
---
# <a name="erroritem-method"></a>Error. Item, метод

Метод **Item** извлекает объект **ерроритем** из очереди ошибок.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

**Число** (**Long**), содержащее индекс объекта **ерроритем** , который требуется получить.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает объект **ерроритем** .

## <a name="remarks"></a>Комментарии

Проигрыватель Windows Media может создавать ряд ошибок в ответ на состояние ошибки. Этот метод позволяет получить конкретную ошибку в очереди, используя номер индекса. Номера индексов для очереди ошибок начинаются с нуля.

Необходимо задать *Параметры*. **енаблиррордиалогс** значение false, если выбрано отображение настраиваемых сообщений об ошибках.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *Ошибка*. Объект **Item** в обработчике событий для предупреждения пользователя о последней ошибке. Объект **Player** создан с идентификатором "Player".


```JScript
<SCRIPT LANGUAGE="JScript"  FOR=Player EVENT=error()>

// Store the most recent error item number.
var max = Player.error.errorCount - 1 

// Store the most recent error in an error item object.
var errItem = Player.error.item(max);

// Use the error item object to store the error info.
errDesc = errItem.errorDescription;
errNum = errItem.errorCode;

// Display the error info.
alert(errNum + "\n" + errDesc);

</SCRIPT> 

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Error**](error-object.md)
</dt> <dt>

[**Объект Ерроритем**](erroritem-object.md)
</dt> </dl>

 

 





