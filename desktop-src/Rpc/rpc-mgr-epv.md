---
title: RPC_MGR_EPV (Рпкдце. h)
description: Тип данных \_ ЕПВ ДИСПЕТЧЕРА RPC \_ определяет вектор точки входа диспетчера.
ms.assetid: 396e76de-065f-471e-ade9-34770b16a958
keywords:
- RPC_MGR_EPV RPC
topic_type:
- apiref
api_name:
- RPC_MGR_EPV
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549ca4b5245b12bda07b46407041a01175955693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801312"
---
# <a name="rpc_mgr_epv"></a>\_ЕПВ ДИСПЕТЧЕРА \_ RPC

Тип данных **\_ \_ ЕПВ диспетчера RPC** определяет вектор точки входа диспетчера.

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a>Элементы

<dl> <dt>

<span id="if-name"></span><span id="IF-NAME"></span>**If-Name**
</dt> <dd>

Указывает имя интерфейса.

</dd> <dt>

<span id="return-type"></span><span id="RETURN-TYPE"></span>**Тип возвращаемого значения**
</dt> <dd>

Указывает тип, возвращаемый функцией **FunctionName** , указанной в IDL-файле.

</dd> <dt>

<span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**FunctionName**
</dt> <dd>

Указывает имя функции, указанной в IDL-файле.

</dd> <dt>

<span id="param-list"></span><span id="PARAM-LIST"></span>**Param-List**
</dt> <dd>

Задает параметры, указанные для функции **FunctionName** в IDL-файле.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Вектор точки входа диспетчера (ЕПВ) является массивом указателей на функции. Массив содержит указатели на реализации функций, указанных в IDL-файле. Число элементов в массиве равно числу функций, указанных в IDL-файле. Приложение может также иметь несколько Епвс, представляющих несколько реализаций функций, указанных в интерфейсе.

Компилятор MIDL создает тип данных **ЕПВ** по умолчанию, именуемый * if-Name ***\_ Server \_ ЕПВ**, где *If-Name* указывает идентификатор интерфейса в файле IDL. Компилятор MIDL Инициализирует этот **ЕПВ** по умолчанию, чтобы он содержал указатели на функции для каждой процедуры, указанной в IDL-файле.

Если сервер предлагает несколько реализаций одного интерфейса, серверное приложение должно объявлять и инициализировать одну переменную типа *If-Name * * * \_ Server \_ ЕПВ** для каждой реализации интерфейса. Каждый **ЕПВ** должен содержать одну точку входа (указатель на функцию) для каждой процедуры, определенной в IDL-файле.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                |
| Заголовок<br/>                   | <dl> <dt>Рпкдце. h (включение RPC. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**рпксерверрегистериф**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[**рпксерверрегистерифекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[**рпксерверунрегистериф**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[**рпксерверунрегистерифекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 





