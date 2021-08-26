---
description: Система передает \_ событие ДБТ девицеарривал Device, когда устройство или носитель вставлены и становятся доступными.
ms.assetid: 8e44cb02-cf79-4b19-807e-20cea07362af
title: Событие DBT_DEVICEARRIVAL (ДБТ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 826d0b510ca76b829eb683396c99579c14a512a6773b76a2049ae7963ede54a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088154"
---
# <a name="dbt_devicearrival-event"></a>\_Событие ДБТ девицеарривал

Система передает \_ событие ДБТ девицеарривал Device, когда устройство или носитель вставлены и становятся доступными.

Чтобы транслировать это событие устройства, система использует сообщение [**WM \_ девицечанже**](wm-devicechange.md) с параметром *wParam* Set ДБТ \_ девицеарривал и *lParam* Set, как описано ниже.


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Дескриптор окна.

</dd> <dt>

*Uiacp* 
</dt> <dd>

Идентификатор сообщения [**WM \_ девицечанже**](wm-devicechange.md) .

</dd> <dt>

*wParam* 
</dt> <dd>

Задайте для параметра значение ДБТ \_ девицеарривал.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру, идентифицирующую вставленное устройство. Структура состоит из независимого от событий заголовка, за которым следуют элементы, зависящие от события, которые описывают устройство. Чтобы использовать эту структуру, рассматривайте структуру как [**\_ \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) -структуру для разработки вещания, а затем проверьте ее член **дбч \_ типа устройства** , чтобы определить тип устройства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true**.

## <a name="remarks"></a>Remarks

Если вставляется носитель, тип поступающих устройств — это том ( **дбч \_ типа устройства** ДБТ \_ девтип \_ Volume), и изменение влияет на носитель (член **дбкв \_ flags** — дбтф \_ Media).

## <a name="examples"></a>Примеры

Пример см. в разделе [обнаружение вставки или удаления носителя](detecting-media-insertion-or-removal.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2003<br/>                                                   |
| Заголовок<br/>                   | <dl> <dt>ДБТ. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[События устройства](device-events.md)
</dt> <dt>

[События управления устройствами](device-management-events.md)
</dt> <dt>

[**расвещание для разработки в \_ \_ HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**WM \_ девицечанже**](wm-devicechange.md)
</dt> </dl>

 

 




