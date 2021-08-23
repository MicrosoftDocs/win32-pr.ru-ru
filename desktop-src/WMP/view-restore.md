---
title: Просмотр. Восстановление
description: Метод Restore восстанавливает представление.
ms.assetid: 8005c14e-771b-4f20-8039-fc09869dc726
keywords:
- просмотреть. восстановление проигрыватель Windows Media
topic_type:
- apiref
api_name:
- VIEW.restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4bb4948c9c21b87ede4c88c85d2fc7681335a2bf6adb32bfa5c51638b773e74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615374"
---
# <a name="viewrestore"></a>Просмотр. Восстановление

Метод **RESTORE** восстанавливает **представление**.

``` syntax
        elementID.restore()
```

## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="examples"></a>Примеры


```JScript
<THEME>
  <VIEW id="View1">
    <BUTTON id="Open" image="Open.png" 
        onclick="jscript:View1.restore()">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**VIEW, элемент**](view-element.md)
</dt> </dl>

 

 





