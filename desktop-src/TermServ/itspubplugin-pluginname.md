---
title: Итспубплугин pluginName, свойство
description: Возвращает имя подключаемого модуля.
ms.assetid: c1ea46b6-fac6-4140-a278-cb04ee9af739
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства pluginName
- службы удаленных рабочих столов свойства pluginName, интерфейс Итспубплугин
- Службы удаленных рабочих столов интерфейса Итспубплугин, свойство pluginName
topic_type:
- apiref
api_name:
- ItsPubPlugin.pluginName
- ItsPubPlugin.get_pluginName
api_location:
- Cpubplugin.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa1cd3103e901255a6226db3e128e81bb17c02e6b586a48ca434ed44932861c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128643"
---
# <a name="itspubpluginpluginname-property"></a>Итспубплугин: свойство Лугиннаме:p

Возвращает имя подключаемого модуля.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_pluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Значение свойства

Указатель на переменную **BSTR** , чтобы получить имя подключаемого модуля.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                         |
| IDL<br/>                      | <dl> <dt>Кпубплугин. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**итспубплугин**](/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin)
</dt> </dl>

 

 





