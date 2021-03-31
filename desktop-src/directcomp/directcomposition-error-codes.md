---
title: Коды ошибок DirectComposition (Дкомп. h)
description: В этом разделе описываются коды ошибок, которые относятся к DirectComposition.
ms.assetid: 8DFBFC34-DBD0-4731-8305-B33E90C96C54
topic_type:
- apiref
api_name:
- DCOMPOSITION_ERROR_ACCESS_DENIED
- DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED
- DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED
- DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED
api_location:
- Dcomp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a76a7527bacf8caa756a0fad75ca70f4bf9a77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136707"
---
# <a name="directcomposition-error-codes"></a>Коды ошибок DirectComposition

При возникновении ошибки Microsoft DirectComposition возвращает код в виде значения **HRESULT** . В этом разделе описываются коды ошибок, которые относятся к DirectComposition. Список общих кодов ошибок модели COM см. в разделе [коды ошибок COM](/windows/desktop/com/com-error-codes).

<dl> <dt>

<span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**\_доступ к ошибке дкомпоситион \_ \_ запрещен**
</dt> <dd> <dl> <dt>


</dt> <dt>



Обработчик окна, указанный в вызове метода [**идкомпоситиондевице:: креатетаржетфорхвнд**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) , принадлежит другому процессу, создавшему объект устройства.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**\_ \_ отображается поверхность ошибки \_ дкомпоситион \_**
</dt> <dd> <dl> <dt>


</dt> <dt>



Поверхность уже была отображена, когда приложение вызвало метод [**идкомпоситионсурфаце:: бегиндрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**Идкомпоситионсурфаце:: суспенддрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)или [**идкомпоситионсурфаце:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) . Дополнительные сведения см. в подразделе "Примечания".


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**\_поверхность ошибки \_ дкомпоситион \_ не \_ \_ готовится к просмотру**
</dt> <dd> <dl> <dt>


</dt> <dt>



Приложение вызвало метод [**идкомпоситионсурфаце:: суспенддрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**Идкомпоситионсурфаце:: ресумедрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)или [**идкомпоситионсурфаце:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) для поверхности, которая не подготавливается к просмотру. Дополнительные сведения см. в подразделе "Примечания".


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**ДКОМПОСИТИОН \_ \_ окно ошибок \_ уже \_ состояло**
</dt> <dd> <dl> <dt>


</dt> <dt>



Метод [**идкомпоситиондевице:: креатетаржетфорхвнд**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) был вызван с *HWND* и *верхними* параметрами, для которых уже существует визуальное дерево.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Если вызов [**идкомпоситионсурфаце:: бегиндрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) был последним действием:



| Вызов этого метода:                                    | Возвращает это значение:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**бегиндрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_ \_ отображается поверхность ошибки \_ дкомпоситион \_** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | \_ОК                                             |
| [**суспенддрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | \_ОК                                             |
| [**ресумедрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **\_ \_ отображается поверхность ошибки \_ дкомпоситион \_** |



 

Если вызов [**идкомпоситионсурфаце:: суспенддрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) был последним действием:



| Вызов этого метода:                                    | Возвращает это значение:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**бегиндрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_ \_ отображается поверхность ошибки \_ дкомпоситион \_** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | \_ОК                                             |
| [**суспенддрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **\_ \_ отображается поверхность ошибки \_ дкомпоситион \_** |
| [**ресумедрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | \_ОК                                             |



 

Если вызов [**идкомпоситионсурфаце:: ресумедрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) был последним действием:



| Вызов этого метода:                                    | Возвращает это значение:                                |
|---------------------------------------------------------|----------------------------------------------------|
| [**бегиндрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_ \_ отображается поверхность ошибки \_ дкомпоситион \_**  |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | \_ОК                                              |
| [**суспенддрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | \_ОК                                              |
| [**ресумедрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **\_ \_ отображается поверхность ошибки \_ дкомпоситион \_ .** |



 

Если вызов [**идкомпоситионсурфаце:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) был последним действием:



| Вызов этого метода:                                    | Возвращает это значение:                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [**бегиндрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | \_ОК                                                   |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | **\_поверхность ошибки \_ дкомпоситион \_ не \_ \_ отображается.** |
| [**суспенддрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **\_поверхность ошибки \_ дкомпоситион \_ не \_ \_ отображается.** |
| [**ресумедрав**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **\_поверхность ошибки \_ дкомпоситион \_ не \_ \_ отображается.** |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                               |
| Header<br/>                   | <dl> <dt>Дкомп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по DirectComposition](reference.md)
</dt> </dl>

 

