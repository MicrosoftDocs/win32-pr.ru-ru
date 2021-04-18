---
description: Определяет тип запроса.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: Перечисление D3DQUERYTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DQUERYTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 21cb3e2f2254d54caacd4217d3e0023446a0c6f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703834"
---
# <a name="d3dquerytype-enumeration"></a>Перечисление D3DQUERYTYPE

Определяет тип запроса. Дополнительные сведения о запросах см. в разделе [запросы (Direct3D 9)](queries.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DQUERYTYPE { 
  D3DQUERYTYPE_VCACHE             = 4,
  D3DQUERYTYPE_ResourceManager    = 5,
  D3DQUERYTYPE_VERTEXSTATS        = 6,
  D3DQUERYTYPE_EVENT              = 8,
  D3DQUERYTYPE_OCCLUSION          = 9,
  D3DQUERYTYPE_TIMESTAMP          = 10,
  D3DQUERYTYPE_TIMESTAMPDISJOINT  = 11,
  D3DQUERYTYPE_TIMESTAMPFREQ      = 12,
  D3DQUERYTYPE_PIPELINETIMINGS    = 13,
  D3DQUERYTYPE_INTERFACETIMINGS   = 14,
  D3DQUERYTYPE_VERTEXTIMINGS      = 15,
  D3DQUERYTYPE_PIXELTIMINGS       = 16,
  D3DQUERYTYPE_BANDWIDTHTIMINGS   = 17,
  D3DQUERYTYPE_CACHEUTILIZATION   = 18,
  D3DQUERYTYPE_MEMORYPRESSURE     = 19
} D3DQUERYTYPE, *LPD3DQUERYTYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE \_ вкаче**
</dt> <dd>

Запрос подсказок к драйверу о структуре данных для кэширования вершин.

</dd> <dt>

<span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE \_ ResourceManager**
</dt> <dd>

Запросите диспетчер ресурсов. Для этого запроса флаги поведения устройства должны включать [D3DCREATE \_ Отключить \_ \_ Управление драйверами](d3dcreate.md).

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ вертексстатс**
</dt> <dd>

Запрос статистики вершин.

</dd> <dt>

<span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**\_Событие D3DQUERYTYPE**
</dt> <dd>

Запрос всех и всех асинхронных событий, выданных из вызовов API.

</dd> <dt>

<span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE \_ перекрытия**
</dt> <dd>

Запрос перекрытия возвращает число пикселей, пройденных в z-тестировании. Эти Пиксели используются для примитивов, выводимых между выпуском [**D3DISSUE \_ Begin**](d3dissue-begin.md) и [**D3DISSUE \_ End**](d3dissue-end.md). Это позволяет приложению проверить результат перекрытия на 0. Ноль полностью перекрыто, что означает, что Пиксели не видны в текущей положении камеры.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**\_Отметка времени D3DQUERYTYPE**
</dt> <dd>

Возвращает 64-разрядную отметку времени.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE \_ тиместампдисжоинт**
</dt> <dd>

Используйте этот запрос для уведомления приложения, если частота счетчика изменилась с \_ метки времени D3DQUERYTYPE.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE \_ тиместампфрек**
</dt> <dd>

Этот результат запроса имеет **значение true** , если значения из \_ запросов отметок времени D3DQUERYTYPE не могут быть непрерывными в течение всего времени \_ запроса D3DQUERYTYPE тиместампдисжоинт. В противном случае результат запроса будет иметь **значение false**.

</dd> <dt>

<span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE \_ пипелинетимингс**
</dt> <dd>

Процент времени обработки данных конвейера.

</dd> <dt>

<span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE \_ интерфацетимингс**
</dt> <dd>

Процент времени обработки данных в драйвере.

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE \_ вертекстимингс**
</dt> <dd>

Процент времени обработки данных шейдера вершин.

</dd> <dt>

<span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE \_ пикселтимингс**
</dt> <dd>

Процент времени обработки данных шейдера пикселей.

</dd> <dt>

<span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ бандвидстимингс**
</dt> <dd>

Сравнения измерений пропускной способности помогают понять производительность приложения.

</dd> <dt>

<span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ качеутилизатион**
</dt> <dd>

Измеряет производительность скорости попадания в кэш для текстур и индексированных вершин.

</dd> <dt>

<span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ меморипрессуре**
</dt> <dd>

Эффективность выделения памяти, содержащейся в структуре [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .



|                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Различия между Direct3D 9 и Direct3D 9Ex:<br/> D3DQUERYTYPE \_ меморипрессуре доступен только в Direct3D9Ex, работающем в Windows 7 (или более текущей операционной системе).<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9:: CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
