---
title: Итссбклиентконнектион, свойство среды
description: Извлекает объект, содержащий сведения о среде, в которой размещен конечный компьютер.
ms.assetid: 97fe4851-96a9-4b23-8ad7-f42b87c655d0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства среды
- Свойство окружения службы удаленных рабочих столов, интерфейс Итссбклиентконнектион
- Службы удаленных рабочих столов интерфейса Итссбклиентконнектион, свойство Environment
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Environment
- ITsSbClientConnection.get_Environment
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33cc1c3c8a13a21135ee834950e8c0a60d2794cd4b1edb618e5e67c0744fe3e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072214"
---
# <a name="itssbclientconnectionenvironment-property"></a>Свойство Итссбклиентконнектион:: Environment

Извлекает объект, содержащий сведения о среде, в которой размещен конечный компьютер. Например, в сценарии виртуального рабочего стола этот объект будет содержать сведения о компьютере, на котором размещена виртуальная машина.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Environment(
  [out, retval] ITsSbEnvironment **ppEnvironment
);
```



## <a name="property-value"></a>Значение свойства

Указатель на указатель на объект среды [**итссбенвиронмент**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) .

## <a name="error-codes"></a>Коды ошибок

Если метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается значение **HRESULT** , указывающее на ошибку. Возможные значения включают, но не ограничиваются, перечисленные в следующем списке.

<dl> <dt>

\_указатель E
</dt> <dd>

Среда не найдена.

</dd> </dl>

## <a name="remarks"></a>Remarks

Подключаемый модуль оркестрации может вызывать этот метод для получения сведений о среде для целевой виртуальной машины.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Сбтсв. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**итссбклиентконнектион**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

 





