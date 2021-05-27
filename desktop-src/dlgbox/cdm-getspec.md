---
title: Сообщение CDM_GETSPEC (Коммдлг. h)
description: Извлекает имя файла (не включая путь) текущего выбранного файла в диалоговом окне Обозреватель — открытие или сохранение как.
ms.assetid: 22a67c92-bd24-4cba-bef8-291d241e6ec8
keywords:
- CDM_GETSPEC диалоговых окон сообщений
topic_type:
- apiref
api_name:
- CDM_GETSPEC
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27eff7e9a14f39554fa6c1a69846bbaca7c39990
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548879"
---
# <a name="cdm_getspec-message"></a>\_Сообщение CDM

\[Начиная с Windows Vista, диалоговые окна " **Открыть** " и " **Сохранить как** " были заменены [диалоговым окном общих элементов](../shell/common-file-dialog.md). Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]

Извлекает имя файла (не включая путь) текущего выбранного файла в диалоговом окне Обозреватель — **Открытие** или **Сохранение как** . Диалоговое окно должно быть создано с флагом **\_ обозревателя ОФН** . в противном случае произойдет сбой сообщения.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETSPEC             (CDM_FIRST + 0x0000)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Размер буфера *lParam* в символах.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на буфер, который получает имя файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если сообщение завершается удачно, возвращаемое значение представляет собой размер (в символах) строки имени файла, включая завершающий нуль-символ. Это либо количество байтов или символов, скопированных в буфер, либо требуемый размер буфера, если буфер слишком мал.

При возникновении ошибки возвращаемое значение меньше нуля.

## <a name="remarks"></a>Комментарии

Соответствующий макрос выглядит следующим образом:

``` syntax
int CommDlg_OpenSave_GetSpec(hwnd, lparam, wparam); 
```

## <a name="requirements"></a>Требования



| Требование | Применение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Коммдлг. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылка**
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

