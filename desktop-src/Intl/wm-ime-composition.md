---
description: Отправляется в приложение, когда редактор IME изменяет состояние композиции в результате нажатия клавиши. Окно получает это сообщение через функцию WindowProc.
ms.assetid: 6de1c4c2-d910-487c-8b82-408cb6e02c44
title: Сообщение WM_IME_COMPOSITION (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d795c1e270be978927e3b93743de5fece7021b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999684"
---
# <a name="wm_ime_composition-message"></a>\_ \_ Сообщение композиции IME WM

Отправляется в приложение, когда редактор IME изменяет состояние композиции в результате нажатия клавиши. Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,     
  WM_IME_COMPOSITION,   
  WPARAM wParam,
  LPARAM lParam          
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Маркер для окна.

</dd> <dt>

*wParam* 
</dt> <dd>

Символ DBCS, представляющий Последнее изменение в строке композиции.

</dd> <dt>

*lParam* 
</dt> <dd>

Значение, указывающее, как изменилась строка композиции или символ. Этот параметр может принимать одно или несколько следующих значений. Дополнительные сведения об этих значениях см. в разделе [строковые значения композиции IME](ime-composition-string-values.md).

<dl><span id="GCS_COMPATTR"></span><span id="gcs_compattr"></span><dt>

**\_КОМПАТТР GC**
</dt><span id="GCS_COMPCLAUSE"></span><span id="gcs_compclause"></span><dt>

**\_КОМПКЛАУСЕ GC**
</dt><span id="GCS_COMPREADSTR"></span><span id="gcs_compreadstr"></span><dt>

**\_КОМПРЕАДСТР GC**
</dt><span id="GCS_COMPREADATTR"></span><span id="gcs_compreadattr"></span><dt>

**\_КОМПРЕАДАТТР GC**
</dt><span id="GCS_COMPREADCLAUSE"></span><span id="gcs_compreadclause"></span><dt>

**\_КОМПРЕАДКЛАУСЕ GC**
</dt><span id="GCS_COMPSTR"></span><span id="gcs_compstr"></span><dt>

**\_КОМПСТР GC**
</dt><span id="GCS_CURSORPOS"></span><span id="gcs_cursorpos"></span><dt>

**\_КУРСОРПОС GC**
</dt><span id="GCS_DELTASTART"></span><span id="gcs_deltastart"></span><dt>

**\_ДЕЛТАСТАРТ GC**
</dt><span id="GCS_RESULTCLAUSE"></span><span id="gcs_resultclause"></span><dt>

**\_РЕСУЛТКЛАУСЕ GC**
</dt><span id="GCS_RESULTREADCLAUSE"></span><span id="gcs_resultreadclause"></span><dt>

**\_РЕСУЛТРЕАДКЛАУСЕ GC**
</dt><span id="GCS_RESULTREADSTR"></span><span id="gcs_resultreadstr"></span><dt>

**\_РЕСУЛТРЕАДСТР GC**
</dt><span id="GCS_RESULTSTR"></span><span id="gcs_resultstr"></span><dt>

**\_РЕСУЛТСТР GC**
</dt> </dl>

Параметр *lParam* также может иметь одно или несколько из следующих значений.



| Значение                                                                                                                                                            | Значение                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CS_INSERTCHAR"></span><span id="cs_insertchar"></span><dl> <dt>**CS \_ инсертчар**</dt> </dl>    | Вставка символа композиции *wParam* в текущей точке вставки. Приложение должно отображать символ композиции, если он обрабатывает это сообщение.<br/>                                                                                                                                                                                                                                |
| <span id="CS_NOMOVECARET"></span><span id="cs_nomovecaret"></span><dl> <dt>**CS \_ номовекарет**</dt> </dl> | Не перемещайте положение курсора в результате обработки сообщения. Например, если редактор IME задает сочетание CS \_ инсертчар и CS \_ номовекарет, приложение должно вставить указанный символ в текущую положение курсора, но не должен перемещать курсор к следующей позиции. Последующее \_ сообщение композиции редактора WM IME \_ с GC \_ ресултстр заменит этот символ.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не имеет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Приложение должно обработать это сообщение, если оно отображает сами символы композиции. В противном случае он должен отправить сообщение в окно IME.

Если приложение создало окно IME, оно должно передать это сообщение в это окно. Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  обрабатывает это сообщение, передавая его в окно IME по умолчанию. Окно IME обрабатывает это сообщение, обновляя его внешний вид в зависимости от указанного флага изменения. Приложение может вызвать [**иммжеткомпоситионстринг**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) для получения нового состояния композиции.

Если ни одно из значений глобальных каталогов \_ не задано, сообщение указывает, что Текущая композиция отменена, и приложения, которые рисуют строку композиции, должны удалить строку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                                                                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                                                                                                      |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h); </dt> <dt>IMM. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Диспетчер метода ввода](input-method-manager.md)
</dt> <dt>

[Сообщения диспетчера методов ввода](input-method-manager-messages.md)
</dt> <dt>

[**иммжеткомпоситионстринг**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)
</dt> </dl>

 

 
