---
title: Структура CD3DX12_PACKED_MIP_INFO (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать D3D12 \_ упакованную \_ \_ информационную структуру MIP.
ms.assetid: B3549D78-C354-48FC-A012-1F835DBD585E
keywords:
- Структура CD3DX12_PACKED_MIP_INFO
topic_type:
- apiref
api_name:
- CD3DX12_PACKED_MIP_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b32a4b0516560ac553b3ce6acb6972def5d0e3f84a2eb84026a0635f779a2c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752164"
---
# <a name="cd3dx12_packed_mip_info-structure"></a>CD3DX12 \_ упакованная \_ \_ информационная структура MIP

Вспомогательная структура, позволяющая легко инициализировать [**D3D12 \_ упакованную \_ \_ информационную структуру MIP**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PACKED_MIP_INFO  : public D3D12_PACKED_MIP_INFO{
   CD3DX12_PACKED_MIP_INFO();
   explicit CD3DX12_PACKED_MIP_INFO(const D3D12_PACKED_MIP_INFO &o);
   CD3DX12_PACKED_MIP_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource);
   operator const D3D12_PACKED_MIP_INFO&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12 \_ Упакованные \_ MIP \_ info ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр CD3DX12 \_ \_ \_ сведений о MIP.

</dd> <dt>

**явные CD3DX12 \_ Упакованные \_ \_ сведения о MIP (const D3D12 \_ упакованный \_ MIP \_ info &o)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ упакованной \_ \_ информации MIP, инициализированной с содержимым другой [**D3D12 \_ упакованной структуры \_ \_ сведений MIP**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .

</dd> <dt>

**CD3DX12 \_ Упакованные \_ \_ сведения о MIP (UINT8 Нумстандардмипс, UINT8 Нумпаккедмипс, UINT Нумтилесфорпаккедмипс, uint старттилеиндексиновераллресаурце)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ упакованных \_ \_ сведений о MIP, инициализируя следующие параметры:

UINT8 Нумстандардмипс

UINT8 Нумпаккедмипс

UINT Нумтилесфорпаккедмипс

UINT Старттилеиндексиновераллресаурце

</dd> <dt>

**Оператор const D3D12 \_ Упакованные \_ MIP \_ info& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ Сведения о упакованных MIP D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





