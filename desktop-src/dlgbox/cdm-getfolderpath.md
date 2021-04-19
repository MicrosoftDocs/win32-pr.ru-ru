---
title: Сообщение CDM_GETFOLDERPATH (Коммдлг. h)
description: Возвращает путь к открытой в данный момент папке или каталогу для диалогового окна "Открыть" или "Сохранить как" в стиле обозревателя.
ms.assetid: 7c3d4598-b45d-46c1-ad0d-cb0ecd20b3eb
keywords:
- CDM_GETFOLDERPATH диалоговых окон сообщений
topic_type:
- apiref
api_name:
- CDM_GETFOLDERPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd6a824892b1a3a31339e36e6a783bb00c08534
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590941"
---
# <a name="cdm_getfolderpath-message"></a>\_Сообщение CDM GETFOLDERPATH

\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](/windows/win32/shell/common-file-dialog). Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]

Возвращает путь к открытой в данный момент папке или каталогу для диалогового окна " **Открыть** " или " **Сохранить как** " в стиле обозревателя. Диалоговое окно должно быть создано с флагом **\_ обозревателя ОФН** . в противном случае произойдет сбой сообщения.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERPATH       (CDM_FIRST + 0x0002)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Размер буфера *lParam* в символах.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на буфер, который получает путь.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если сообщение завершается удачно, возвращаемое значение представляет собой размер (в символах) строки пути, включая завершающий нуль-символ. Это либо количество байтов или символов, скопированных в буфер, либо требуемый размер буфера, если буфер слишком мал.

При возникновении ошибки возвращаемое значение меньше нуля.

## <a name="remarks"></a>Замечания

Соответствующий макрос выглядит следующим образом:

``` syntax
int CommDlg_OpenSave_GetFolderPath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Коммдлг. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**жетсавефиленаме**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

**Зрения**
</dt> <dt>

[Библиотека общих диалоговых окон](common-dialog-box-library.md)
</dt> </dl>

 

