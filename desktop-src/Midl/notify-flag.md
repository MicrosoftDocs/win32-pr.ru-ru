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
ms.openlocfilehash: af61999f0527b599cf358c38288a8c67473445a9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068826"
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

## <a name="remarks"></a>Комментарии

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

 

 




