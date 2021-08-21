---
title: Структура CD3DX12_BLEND_DESC (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать структуру D3D12 \_ Blend \_ DESC.
ms.assetid: D37BB62E-904B-4953-9119-21F3B37570C0
keywords:
- Структура CD3DX12_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40acdedbe428d808a576b68645a3e662dc71389b4d6dd0c19424278f28deb93a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989954"
---
# <a name="cd3dx12_blend_desc-structure"></a>\_ \_ Структура DESC CD3DX12 Blend

Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12 \_ Blend \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_BLEND_DESC  : public D3D12_BLEND_DESC{
   CD3DX12_BLEND_DESC();
   explicit CD3DX12_BLEND_DESC(const D3D12_BLEND_DESC& o);
   explicit CD3DX12_BLEND_DESC(CD3DX12_DEFAULT);
   ~CD3DX12_BLEND_DESC();
   operator const D3D12_BLEND_DESC&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12 \_ Blend \_ DESC ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр экземпляра CD3DX12 \_ Blend \_ DESC.

</dd> <dt>

**явное CD3DX12 \_ Blend \_ DESC (const D3D12 \_ Blend \_ DESC& o)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ Blend \_ DESC, инициализированный с содержимым другой структуры [**D3D12 \_ Blend \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .

</dd> <dt>

**явное CD3DX12 \_ Blend \_ DESC (CD3DX12 \_ по умолчанию)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ Blend \_ DESC, инициализируемый параметрами по умолчанию.



| Состояние                                   | Значение по умолчанию                    |
|-----------------------------------------|----------------------------------|
| алфатоковеражеенабле                   | **FALSE**                        |
| индепендентбленденабле                  | **FALSE**                        |
| Рендертаржет \[ 0 \] . бленденабле           | **FALSE**                        |
| Рендертаржет \[ 0 \] . логикопенабле         | **FALSE**                        |
| Рендертаржет \[ 0 \] . сркбленд              | D3D12 \_ Blend ( \_ один)                |
| Рендертаржет \[ 0 \] . дестбленд             | D3D12 \_ Blend \_ 0               |
| Рендертаржет \[ 0 \] . блендоп               | \_Добавление D3D12 Blend \_ Op \_            |
| Рендертаржет \[ 0 \] . сркблендалфа         | D3D12 \_ Blend ( \_ один)                |
| Рендертаржет \[ 0 \] . дестблендалфа        | D3D12 \_ Blend \_ 0               |
| Рендертаржет \[ 0 \] . блендопалфа          | \_Добавление D3D12 Blend \_ Op \_            |
| Рендертаржет \[ 0 \] . логикоп               | D3D12 \_ Logic \_ Op \_           |
| Рендертаржет \[ 0 \] . рендертаржетвритемаск | D3D12 \_ Цвет \_ записи \_ включить \_ все |



 

</dd> <dt>

**~ CD3DX12 \_ Blend \_ DESC ()**
</dt> <dd>

Уничтожает экземпляр CD3DX12 \_ Blend \_ DESC.

</dd> <dt>

**Константа operator const D3D12 \_ Blend \_ DESC& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**D3D12 \_ Blend, \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





