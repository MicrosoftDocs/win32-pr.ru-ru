---
title: Структура CD3DX12_GPU_DESCRIPTOR_HANDLE (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ \_ \_ структуры дескриптора GPU D3D12.
ms.assetid: 6E405AD6-D370-4B87-849A-C52D64C79BF7
keywords:
- Структура CD3DX12_GPU_DESCRIPTOR_HANDLE
topic_type:
- apiref
api_name:
- CD3DX12_GPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429d41d401b7d3e928bc4ab76850b36ae41b1e8a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703679"
---
# <a name="cd3dx12_gpu_descriptor_handle-structure"></a>\_ \_ \_ Структура ДЕСКРИПТОРа GPU CD3DX12

Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ \_ \_ дескриптора GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_GPU_DESCRIPTOR_HANDLE  : public D3D12_GPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            inline operator==( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  bool                            inline operator!=( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_GPU_DESCRIPTOR_HANDLE & operator=(const D3D12_GPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Дескриптор CD3DX12 \_ GPU \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ \_ \_ дескриптора CD3DX12 GPU.

</dd> <dt>

**явный дескриптор \_ GPU \_ CD3DX12 \_ (константа дескриптора gpu const D3D12 \_ \_ \_ &o)**
</dt> <dd>

Создает новый экземпляр \_ \_ дескриптора дескриптора GPU CD3DX12 \_ , инициализированного с содержимым другой структуры [**\_ \_ \_ дескриптора GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) .

</dd> <dt>

**\_Дескриптор CD3DX12 \_ GPU \_ ( \_ по умолчанию CD3DX12)**
</dt> <dd>

Создает новый экземпляр \_ \_ дескриптора дескриптора GPU CD3DX12 \_ , инициализируемый параметрами по умолчанию (устанавливает указатель на нуль).

</dd> <dt>

**Дескриптор \_ GPU \_ CD3DX12 \_ (константа дескриптора gpu const D3D12 \_ \_ \_ &other, int оффсетскаледбинкрементсизе)**
</dt> <dd>

Создает новый экземпляр \_ \_ дескриптора дескриптора GPU CD3DX12 \_ , инициализируя следующие параметры:

\_Дескриптор GPU \_ D3D12 \_ &другой

INT Оффсетскаледбинкрементсизе: число инкрементов, на которое смещается смещение.

</dd> <dt>

**Дескриптор \_ GPU \_ CD3DX12 \_ (константа дескриптора gpu const D3D12 \_ \_ \_ &other, int оффсетиндескрипторс, uint дескрипторинкрементсизе)**
</dt> <dd>

Создает новый экземпляр \_ \_ дескриптора дескриптора GPU CD3DX12 \_ , инициализируя следующие параметры:

\_Дескриптор GPU \_ D3D12 \_ &другой

INT Оффсетиндескрипторс: количество дескрипторов, с помощью которых увеличивается значение.

UINT Дескрипторинкрементсизе: величина приращения для каждого дескриптора, включая заполнение.

</dd> <dt>

**Offset (INT Оффсетиндескрипторс, UINT Дескрипторинкрементсизе)**
</dt> <dd>

Задает смещение на основе указанного числа дескрипторов и величины приращения каждого из них. Использует следующие параметры:

INT Оффсетиндескрипторс: количество дескрипторов, с помощью которых увеличивается значение.

UINT Дескрипторинкрементсизе: величина приращения для каждого дескриптора, включая заполнение.

</dd> <dt>

**Offset (INT Оффсетскаледбинкрементсизе)**
</dt> <dd>

Задает смещение на основе указанного числа приращений. Использует следующие параметры:

INT Оффсетскаледбинкрементсизе: число инкрементов, на которое смещается смещение.

</dd> <dt>

**встроенный оператор = = ( \_ в \_ константе дескриптора \_ GPU D3D12 \_ \_& Other) const**
</dt> <dd>

Проверяет на равенство между текущим \_ дескриптором CD3DX12 GPU и заданным дескриптором дескриптора \_ \_ GPU D3D12 или дескриптором \_ \_ \_ CD3DX12 \_ \_ \_ маркера GPU.

</dd> <dt>

**встроенный оператор! = ( \_ в const D3D12 дескриптора GPU дескриптора \_ \_ \_ \_& Other) const**
</dt> <dd>

Проверяет наличие неравенства между текущим \_ дескриптором CD3DX12 GPU \_ и заданным дескриптором дескриптора \_ GPU D3D12 или дескриптором \_ \_ \_ CD3DX12 \_ \_ \_ маркера GPU.

</dd> <dt>

**operator = (const D3D12 дескриптор GPU дескриптора \_ графического процессора \_ \_ &Other)**
</dt> <dd>

Задает \_ \_ дескриптору текущего дескриптора GPU CD3DX12 \_ те же значения, что и указанный \_ дескриптор D3D12 или дескриптор GPU \_ \_ CD3DX12 \_ \_ \_ .

</dd> <dt>

**Встроенный Инитоффсеттед ( \_ в \_ \_ \_ дескрипторе дескриптора GPU const D3D12 \_ &Base, int оффсетскаледбинкрементсизе)**
</dt> <dd>

Инициализирует структуру [**\_ \_ \_ дескриптора GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) с указанным числом элементов. Использует следующие параметры:

\_В \_ const D3D12 дескриптора GPU дескриптора \_ \_ \_ &Base: базовый адрес, по которому производится смещение.

INT Оффсетскаледбинкрементсизе: число инкрементов, на которое смещается смещение.

</dd> <dt>

**Встроенный Инитоффсеттед ( \_ в \_ \_ \_ дескрипторе дескриптора GPU const D3D12 \_ &Base, int оффсетиндескрипторс, uint дескрипторинкрементсизе)**
</dt> <dd>

Инициализирует структуру [**\_ \_ \_ дескриптора GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) со смещением, используя указанное число дескрипторов заданного размера. Использует следующие параметры:

\_В \_ const D3D12 дескриптора GPU дескриптора \_ \_ \_ &Base: базовый адрес, по которому производится смещение.

INT Оффсетиндескрипторс: количество дескрипторов, по которым производится смещение.

UINT Дескрипторинкрементсизе: величина приращения для каждого дескриптора, включая заполнение.

</dd> <dt>

**статический встроенный Инитоффсеттед ( \_ out D3D12 Handle дескриптор \_ gpu дескриптор \_ \_ \_ &, в константном дескрипторе дескриптора \_ \_ \_ GPU D3D12 \_ \_ &Base, int оффсетскаледбинкрементсизе)**
</dt> <dd>

Инициализирует структуру [**\_ \_ \_ дескриптора GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) со смещением, используя указанное число дескрипторов заданного размера. Использует следующие параметры:

\_Выходной дескриптор GPU дескриптора D3D12 дескриптора \_ \_ \_ \_ &: выводит полученный \_ дескриптор GPU D3D12 \_ \_ .

\_В \_ const D3D12 дескриптора GPU дескриптора \_ \_ \_ &Base: базовый адрес, по которому производится смещение.

INT Оффсетскаледбинкрементсизе: число инкрементов, на которое смещается смещение.

</dd> <dt>

**статический встроенный Инитоффсеттед ( \_ out D3D12 Handle дескриптор \_ \_ GPU \_ \_ &дескриптор, в дескрипторе \_ \_ \_ \_ маркера GPU D3D12 \_ &Base, int оффсетиндескрипторс, uint дескрипторинкрементсизе)**
</dt> <dd>

Инициализирует структуру [**\_ \_ \_ дескриптора GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) со смещением, используя указанное число дескрипторов заданного размера. Использует следующие параметры:

\_Выходной дескриптор GPU дескриптора D3D12 дескриптора \_ \_ \_ \_ &: выводит полученный \_ дескриптор GPU D3D12 \_ \_ .

\_В \_ const D3D12 дескриптора GPU дескриптора \_ \_ \_ &Base: базовый адрес, по которому производится смещение.

INT Оффсетиндескрипторс: количество дескрипторов, по которым производится смещение.

UINT Дескрипторинкрементсизе: величина приращения для каждого дескриптора, включая заполнение.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Дескриптор D3D12 \_ GPU \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





