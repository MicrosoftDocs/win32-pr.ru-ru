---
description: Закрывает маркер поставщика билетов на печать.
ms.assetid: ce979c89-9f9d-4e89-b142-beed414caa3f
title: Функция Унбиндптпровидерсунк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnbindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: dd87f528603624e9957d8c5f3fb12cc857ec4f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693056"
---
# <a name="unbindptproviderthunk-function"></a>Функция Унбиндптпровидерсунк

\[Эта функция не поддерживается и может быть отключена или удалена в будущих версиях Windows. [**Птклосепровидер**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) предоставляет эквивалентную функциональность, и вместо нее следует использовать.\]

Закрывает маркер поставщика билетов на печать.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UnbindPTProviderThunk(
  _In_ HPTPROVIDER hProvider
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпровидер* \[ окне\]
</dt> <dd>

Маркер открытого поставщика билетов на печать. Этот маркер возвращается функцией [**биндптпровидерсунк**](bindptproviderthunk.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение **\_ ОК**. в противном случае возвращается код ошибки **HRESULT** . Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Схема печати](./printschema.md)
</dt> <dt>

[**птклосепровидер**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)
</dt> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Функции API очереди печати принтера](printing-and-print-spooler-functions.md)
</dt> </dl>

 

