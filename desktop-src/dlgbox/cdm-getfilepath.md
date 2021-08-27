---
title: Сообщение CDM_GETFILEPATH (Коммдлг. h)
description: Получает путь и имя выбранного файла в диалоговом окне Обозреватель — открытие или сохранение как.
ms.assetid: fad8c5e2-9838-45a8-8c51-4326c989d939
keywords:
- CDM_GETFILEPATH диалоговых окон сообщений
topic_type:
- apiref
api_name:
- CDM_GETFILEPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ac18880ef62df1d228c006f0bc33fcf4932cbb976419ee29464e49828d8173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786337"
---
# <a name="cdm_getfilepath-message"></a>Сообщение CDM. \_

\[начиная с Windows Vista общие диалоговые окна " **открыть** " и " **сохранить как** " были заменены [диалоговым окном общих элементов](../shell/common-file-dialog.md). Рекомендуется использовать API-интерфейс общего элемента, а не эти диалоговые окна из библиотеки общих диалоговых окон.\]

Получает путь и имя выбранного файла в диалоговом окне Обозреватель — **Открытие** или **Сохранение как** . Диалоговое окно должно быть создано с флагом **\_ обозревателя ОФН** . в противном случае произойдет сбой сообщения.


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFILEPATH         (CDM_FIRST + 0x0001)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Размер буфера *lParam* в символах. Для версии ANSI это число байтов; для версии Юникода это число символов.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на буфер, который получает имя файла и путь.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если сообщение завершается удачно, возвращаемое значение представляет собой размер (в символах) имени файла и строки пути, включая завершающий нуль-символ. Это либо количество байтов или символов, скопированных в буфер, либо требуемый размер буфера, если буфер слишком мал.

При возникновении ошибки возвращаемое значение меньше нуля.

## <a name="remarks"></a>Remarks

Соответствующий макрос выглядит следующим образом:

``` syntax
int CommDlg_OpenSave_GetFilePath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>коммдлг. h (включает Windows. h)</dt> </dl> |



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

