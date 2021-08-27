---
title: Итссбенвиронмент имя свойства
description: Извлекает значение, указывающее имя среды, в которой размещен конечный компьютер.
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Имя свойства службы удаленных рабочих столов
- Свойство Name службы удаленных рабочих столов, интерфейс Итссбенвиронмент
- Службы удаленных рабочих столов интерфейса Итссбенвиронмент, свойство Name
topic_type:
- apiref
api_name:
- ITsSbEnvironment.Name
- ITsSbEnvironment.get_Name
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d60f64cf8bc350ca80072b2c7a43ecabf2fbe5d4650188b7d5a5e5c05a4fbc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072204"
---
# <a name="itssbenvironmentname-property"></a>Свойство Итссбенвиронмент:: Name

Извлекает значение, указывающее имя среды, в которой размещен конечный компьютер.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Значение свойства

Указатель на переменную **BSTR** , содержащую имя среды.

## <a name="remarks"></a>Remarks

Этот метод возвращает строку, которая не используется напрямую компонентом подключение к удаленному рабочему столу Broker (RDCB). RDCB передает эту строку в подключаемые модули ресурсов.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Сбтсв. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**итссбенвиронмент**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 





