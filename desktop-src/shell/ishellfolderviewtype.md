---
description: Предоставляет методы, позволяющие папке оболочки поддерживать различные представления содержимого (различные иерархические макеты данных).
title: Интерфейс Ишеллфолдервиевтипе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9b597f6b-ef27-4fa1-ad00-e131dbd979e7
ms.openlocfilehash: 1440b6d14950ad70d2c76168b28bb1077b19b5a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080770"
---
# <a name="ishellfolderviewtype-interface"></a>Интерфейс Ишеллфолдервиевтипе

Предоставляет методы, позволяющие папке оболочки поддерживать различные представления содержимого (различные иерархические макеты данных).

## <a name="members"></a>Элементы

Интерфейс **ишеллфолдервиевтипе** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Ишеллфолдервиевтипе** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ишеллфолдервиевтипе** содержит следующие методы.



| Метод                                                                      | Описание                                                                                                                                                          |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**енумвиевс**](ishellfolderviewtype-enumviews.md)                         | Получает перечислитель, возвращающий один ПИДЛ для каждого расширенного представления.<br/>                                                                                |
| [**жетдефаултвиевнаме**](ishellfolderviewtype-getdefaultviewname.md)       | Возвращает имя представления по умолчанию. Вызовите метод [**ишеллфолдер:: жетдисплайнамеоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) , чтобы получить имена других представлений.<br/> |
| [**жетвиевтипепропертиес**](ishellfolderviewtype-getviewtypeproperties.md) | Возвращает свойства представления.<br/>                                                                                                                          |
| [**транслатевиевпидл**](ishellfolderviewtype-translateviewpidl.md)         | Восстанавливает ПИДЛ из одного иерархического представления папки оболочки в другое представление.<br/>                                             |



 

## <a name="remarks"></a>Примечания

Этот перечислитель возвращает PIDL, которые являются специальными скрытыми папками на верхнем уровне папки оболочки, которые в противном случае не перечисляются. Представление по умолчанию — это одна из папок оболочки, отображаемая в обычном режиме.

Этот интерфейс не определен ни в одном из файлов общедоступного заголовка. Если вы решили реализовать этот интерфейс, можно использовать следующий код C/C++ для объявления своих методов.


```
#undef  INTERFACE
#define INTERFACE   IShellFolderViewType
DECLARE_INTERFACE_IID_(IShellFolderViewType, IUnknown, "49422C1E-1C03-11d2-8DAB-0000F87A556C")
{
    // **_ IUnknown methods _*_
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void _*ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // **_ IShellFolderViewType Methods _*_

    // EnumViews:
    //   Returns an enumerator which will give out one pidl for every extended view.
    STDMETHOD(EnumViews)(THIS_ ULONG grfFlags, __out IEnumIDList _*ppenum) PURE;

    // GetDefaultViewName:
    //   Returns the name of the default view.  The names of the other views
    //   can be retrieved by calling GetDisplayNameOf.
    STDMETHOD(GetDefaultViewName)(THIS_ DWORD  uFlags, __out LPWSTR *ppwszName) PURE;
    STDMETHOD(GetViewTypeProperties)(THIS_ PCUITEMID_CHILD pidl, __out DWORD *pdwFlags)  PURE;

    // TranslateViewPidl:
    //   Attempts to take a pidl represented in one hierarchical representation of
    //   the Shell folder, and find it in a different representation.
    //   pidl should be relative to the root folder.
    //   Remember to ILFree ppidlOut
    STDMETHOD(TranslateViewPidl)(THIS_ PCUIDLIST_RELATIVE pidl, PCUIDLIST_RELATIVE pidlView,
              __out PIDLIST_RELATIVE *ppidlOut) PURE;
};

#define SFVTFLAG_NOTIFY_CREATE  0x00000001
#define SFVTFLAG_NOTIFY_RESORT  0x00000002
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
