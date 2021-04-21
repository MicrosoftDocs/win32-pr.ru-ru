---
UID: NF:directml.DMLCreateDevice1
title: Функция DMLCreateDevice1
description: Создает устройство Директмл для данного устройства Direct3D 12.
helpviewer_keywords:
- DMLCreateDevice1
- DMLCreateDevice1 function
- direct3d12.dmlcreatedevice1
- directml/DMLCreateDevice1
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
- DMLCreateDevice1
- directml/DMLCreateDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- DirectML.dll
api_name:
- DMLCreateDevice1
ms.openlocfilehash: f722b12208bd808f01e177feb907f94c33541496
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803772"
---
# <a name="dmlcreatedevice1-function-directmlh"></a>Функция DMLCreateDevice1 (директмл. h)

Создает устройство Директмл для данного устройства Direct3D 12.

> [!IMPORTANT]
> Этот API доступен как часть автономного распространяемого пакета Директмл (см. [Microsoft. AI. директмл](https://www.nuget.org/packages/Microsoft.AI.DirectML/) версии 1,4 и более поздних версий). См. также [Журнал версий директмл](../dml-version-history.md).

## <a name="syntax"></a>Синтаксис

```cpp
HRESULT DMLCreateDevice1(
  ID3D12Device            *d3d12Device,
  DML_CREATE_DEVICE_FLAGS flags,
  DML_FEATURE_LEVEL       minimumFeatureLevel,
  REFIID                  riid,
  void                    **ppv
);
```

## <a name="parameters"></a>Параметры

`d3d12Device`

Тип: <b> <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>*</b>

Указатель на [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) , представляющий устройство Direct3D 12 для создания устройства директмл. Директмл поддерживает любой уровень D3D и устройства Direct3D 12, созданные на любом адаптере, включая деформацию. Однако не все функции в Директмл могут быть доступны в зависимости от возможностей устройства Direct3D 12. Дополнительные сведения см. в разделе [идмлдевице:: чеккфеатуресуппорт](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport) .

Если вызов **DMLCreateDevice1** успешно выполнен, устройство директмл поддерживает строгую ссылку на устройство с Direct3D 12.

`flags`

Тип: <b>DML_CREATE_DEVICE_FLAGS</b>

Значение [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) , указывающее дополнительные параметры создания устройства.

`minimumFeatureLevel`

Тип: <b>DML_FEATURE_LEVEL</b>

Значение [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) , указывающее минимальную необходимую поддержку уровня компонента.

Этот параметр может быть полезен для вызывающих объектов, которым требуется определенная версия Директмл, но кто может найти вызов более старой версии Директмл. Это может произойти, например, когда пользователь запускает приложение в более старой версии Windows 10.

Приложения, которые явно зависят от функциональных возможностей, представленных на определенном уровне функций, могут указывать его как *минимумфеатурелевел*. Это гарантирует, что **DMLCreateDevice1** не будет выполняться, пока базовая реализация *не будет* такой же, как и требуемый минимальный уровень функций.

Обратите внимание, что, поскольку этот параметр указывает *Минимальный* уровень компонента, базовое устройство директмл может поддерживать более высокий уровень функций, чем запрошенный минимум. После завершения создания устройства можно запросить все уровни функций, поддерживаемые этим устройством, с помощью [идмлдевице:: чеккфеатуресуппорт](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).

`riid`

Тип: <b>рефиид</b>

Ссылка на глобальный уникальный идентификатор (GUID) интерфейса, который вы хотите вернуть на <i>устройстве</i>. Это должен быть идентификатор GUID [идмлдевице](/windows/win32/api/directml/nn-directml-idmldevice).

`ppv`

Тип: \_ COM \_ аутптр \_ OPT \_ <b>void * *</b>

Указатель на блок памяти, который получает указатель на устройство. Это адрес указателя на [идмлдевице](/windows/win32/api/directml/nn-directml-idmldevice), представляющий созданное устройство директмл.


## <a name="return-value"></a>Возвращаемое значение

Тип: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

Если функция завершается с ошибкой, она возвращает <b>S_OK</b>. В противном случае возвращается код ошибки [HRESULT](/windows/desktop/winprog/windows-data-types) .

Если эта версия Директмл не поддерживает запрашиваемый *минимумфеатурелевел* , эта функция возвратит **DXGI_ERROR_UNSUPPORTED**.

Для использования отладочных слоев Директмл необходимо установить компонент "графические инструменты" по запросу (FOD). Если флаг [DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) указан в параметре *flags* и отладочные слои не установлены, **DMLCreateDevice1** возвращает **DXGI_ERROR_SDK_COMPONENT_MISSING**.

## <a name="remarks"></a>Комментарии

Более новая версия этой функции, [DMLCreateDevice1](), появилась в директмл версии 1.1.0. **DMLCreateDevice1** эквивалентен вызову **DMLCreateDevice1** и указанию *минимумфеатурелевел* [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).

## <a name="availability"></a>Доступность

Этот API появился в версии Директмл `1.1.0` .

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Целевая платформа** | Windows |
| **Header** | директмл. h |
| **Библиотека** | Директмл. lib |
| **КОМПОНОВКИ** | DirectML.dll |

## <a name="see-also"></a>См. также раздел

* [Перечисление DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [Журнал версий DirectML](../dml-version-history.md)
* [Журнал уровня компонентов DirectML](/windows/win32/direct3d12/dml-feature_level-history)    
* [Использование слоя отладки Директмл](../dml-debug-layer.md)