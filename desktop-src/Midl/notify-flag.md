---
title: атрибут notify_flag
description: Атрибут \ notify \_ флаг \ предоставляет уведомление, определяющее, вызывается ли Серверная подпрограммы.
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- notify_flag атрибута MIDL
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9fb7479667fb9757924dcba765c34138cf01c1ad6645ce7bfdc525be393e77f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066878"
---
# <a name="notify_flag-attribute"></a>\_атрибут флага notify

Атрибут **\[ \_ флага \] Notify** предоставляет уведомление, определяющее, вызывается ли Серверная подпрограммы.

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*имя процедуры* 
</dt> <dd>

Имя удаленной процедуры, с которой \_ связана процедура уведомления об отметке.

</dd> </dl>

## <a name="remarks"></a>Remarks

Атрибут **\[ \_ флага \] Notify** аналогичен применению к атрибуту **\[ Notify \]** .

Имя процедуры **\[ уведомления \_ флаг \]** — это имя удаленной процедуры с суффиксом **\_ Notify \_**. Процедура **\_ \_ флага уведомления** не требует никаких параметров и не возвращает результат. Прототип этой процедуры также создается в файле заголовка. Например, если IDL-файл содержит следующее:

``` syntax
MyProcedure([in] short S);
```

Укажите следующие сведения в ACF для MIDL, чтобы создать вызов **\_ \_ флага уведомления** :

``` syntax
[notify_flag] MyProcedure();
```

Компилятор MIDL создаст код заглушки сервера, который содержит следующий вызов процедуры **\_ уведомления о \_ флаге** :

``` syntax
MyProcedure_notify_flag();
```

Файл заголовка будет содержать прототип:

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

**\_ MIDL \_ Нотифифлаг** имеет **значение true** , если вызывается Серверная подпрограммы.

## <a name="examples"></a>Примеры

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**явлении**](notify.md)
</dt> </dl>

 

 




