---
UID: NF:directml.IDMLDevice1.CompileGraph
title: 'IDMLDevice1:: Компилеграф'
description: Компилирует граф операторов Директмл в объект, который можно отправить в GPU.
helpviewer_keywords:
- CompileGraph
- CompileGraph method
- CompileGraph method
- IDMLDevice1 interface
- IDMLDevice1 interface
- CompileGraph method
- IDMLDevice1.CompileGraph
- IDMLDevice1::CompileGraph
- direct3d12.idmldevice1_compileoperator
- directml/IDMLDevice1::CompileGraph
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1::CompileGraph
- directml/IDMLDevice1::CompileGraph
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.dll
api_name:
- IDMLDevice1.CompileGraph
ms.openlocfilehash: 25dbc62fac9cd38d9728a295e336038441aee19f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719908"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a>Метод IDMLDevice1:: Компилеграф (директмл. h)

Компилирует граф операторов Директмл в объект, который можно отправить в GPU.

Скомпилированный оператор представляет собой эффективную, помогут форму оператора, который подходит для выполнения на GPU. Скомпилированный оператор содержит состояние (например, шейдеры и другие объекты), необходимые для выполнения. Поскольку скомпилированный оператор реализует интерфейс [идмлпажеабле](/windows/win32/api/directml/nn-directml-idmlpageable) , вы можете при необходимости исключить его из памяти GPU. Дополнительные сведения см. в разделе [IDMLDevice1:: вытеснение](/windows/win32/api/directml/nf-directml-idmldevice-evict) и [IDMLDevice1:: макересидент](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) .

Скомпилированный оператор не использует объекты [идмлоператор](/windows/win32/api/directml/nn-directml-idmloperator) , предоставленные в описании графа, и не ссылается на них после того, как этот метод возвращает значение.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис

```cpp
HRESULT CompileGraph(
  const DML_GRAPH_DESC *desc,
  DML_EXECUTION_FLAGS  flags,
  REFIID               riid,
  void                 **ppv
);
```

## <a name="parameters"></a>Параметры

`desc`

Тип: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***

Описание графа для компиляции. См. [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).

`flags`

Тип: [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)

Любые флаги для управления выполнением этого оператора.

`riid`

Тип: <b>рефиид</b>

Ссылка на глобальный уникальный идентификатор (GUID) интерфейса, который вы хотите вернуть в <i>ППВ</i>. Это должен быть идентификатор GUID [идмлкомпиледоператор](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).

`ppv`

Тип: <b>void * *</b>

Указатель на блок памяти, который получает указатель на скомпилированный оператор. Это адрес указателя на [идмлкомпиледоператор](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), представляющий созданный скомпилированный оператор.


## <a name="return-value"></a>Возвращаемое значение

Тип: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

Если этот метод завершается с ошибкой, возвращается **S_OK**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

API Graph оператора Директмл предоставляет абстрактный способ эффективного использования Директмл в различных аппаратных средствах. Директмл применяет оптимизацию на уровне тензорные, например, выбор наиболее эффективного макета тензорные в зависимости от используемого адаптера. Он также применяет оптимизацию, например удаление операторов JOIN или Split.

Перед созданием графа Директмл рекомендуется применить высокоуровневые оптимизации. Например, отказывается от операторов свертки с Батчнорм, сворачиванием констант и общим исключением части выражения. Оптимизация в оптимизаторе графов Директмл предназначена для дополнения таких независимых от устройств оптимизаций, которые обычно обрабатываются универсальными платформами машинного обучения.

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Целевая платформа** | Windows |
| **Header** | директмл. h |
| **Библиотека** | Директмл. lib |
| **КОМПОНОВКИ** | DirectML.dll |

## <a name="see-also"></a>См. также раздел

[IDMLDevice1](/windows/win32/api/directml/nn-directml-idmldevice)