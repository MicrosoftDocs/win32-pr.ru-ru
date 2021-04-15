---
description: Подклассировать все элементы управления в диалоговом окне и в самом диалоговом окне.
ms.assetid: 4d3c298b-07ba-4668-badd-dddecc389e70
title: Функция Ctl3dSubclassDlgEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassDlgEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 6e29f65d5ddc3d0d9a7de05eef88b7a662e0e43f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649033"
---
# <a name="ctl3dsubclassdlgex-function"></a>Функция Ctl3dSubclassDlgEx

Подклассировать все элементы управления в диалоговом окне и в самом диалоговом окне.

## <a name="syntax"></a>Синтаксис


```C++
PUBLIC BOOL FAR PASCAL Ctl3dSubclassDlgEx(
   HWND  hwndDlg,
   DWORD grbit
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хвнддлг* 
</dt> <dd>

Маркер диалогового окна.

</dd> <dt>

*грбит* 
</dt> <dd>

Типы элементов управления, которые должны быть подклассами. Это значение может быть любым из следующих.



| Значение                                                                                                                                                                                                                                     | Значение                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="CTL3D_BUTTONS"></span><span id="ctl3d_buttons"></span><dl> <dt>**CTL3D сегодня \_ КНОПКИ**</dt> <dt>0x0001</dt> </dl>                 | Кнопки подклассов.<br/>                  |
| <span id="CTL3D_LISTBOXES"></span><span id="ctl3d_listboxes"></span><dl> <dt>**CTL3D сегодня \_ СПИСКИ**</dt> <dt>0x0002</dt> </dl>           | Списки подклассов.<br/>               |
| <span id="CTL3D_EDITS"></span><span id="ctl3d_edits"></span><dl> <dt>**CTL3D сегодня \_ РЕДАКТИРУЕТ**</dt> <dt>0x0004</dt> </dl>                       | Элементы управления редактированием подклассов.<br/>            |
| <span id="CTL3D_COMBOS"></span><span id="ctl3d_combos"></span><dl> <dt>**CTL3D сегодня \_ КомБОС**</dt> <dt>0x0008</dt> </dl>                    | Поля со списком подклассов.<br/>              |
| <span id="CTL3D_STATICTEXTS"></span><span id="ctl3d_statictexts"></span><dl> <dt>**CTL3D сегодня \_ СТАТИКТЕКСТС**</dt> <dt>0x0010</dt> </dl>     | Подклассировать статические текстовые элементы управления.<br/>     |
| <span id="CTL3D_STATICFRAMES"></span><span id="ctl3d_staticframes"></span><dl> <dt>**CTL3D сегодня \_ СТАТИКФРАМЕС**</dt> <dt>0x0020</dt> </dl>  | Создать подкласс для статических фреймов.<br/>            |
| <span id="CTL3D_ALL"></span><span id="ctl3d_all"></span><dl> <dt>**CTL3D сегодня \_ ВСЕ**</dt> <dt>0xFFFF</dt> </dl>                             | Подкласс все элементы управления.<br/>             |
| <span id="CTL3D_NODLGWINDOW"></span><span id="ctl3d_nodlgwindow"></span><dl> <dt>**CTL3D сегодня \_ НОДЛГВИНДОВ**</dt> <dt>0x00010000</dt> </dl> | Не подделать подкласс диалогового окна.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если функция выполнена. в противном случае возвращается **значение false**.

## <a name="remarks"></a>Комментарии

Эта функция особенно полезна в приложениях, основанных на C++.

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
