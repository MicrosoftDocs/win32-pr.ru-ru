---
title: Функция обратного вызова Транслатедиспатч
description: Используется клиентом функции Дореадермоде для перехвата и явной обработки сообщений Windows, предназначенных для области прокрутки окна режима чтения. Это функция обратного вызова, определяемая приложением.
ms.assetid: a50cff4f-ae10-4c3c-a386-9ec7c7d6256f
keywords:
- функции обратного вызова транслатедиспатч Windows элементы управления
topic_type:
- apiref
api_name:
- TranslateDispatch
- PFNREADERTRANSLATEDISPATCH
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08f726c3f56579260e96a882f1123d035df37cb3f7f71fd0ecbc47d41672359c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060534"
---
# <a name="translatedispatch-callback-function"></a>Функция обратного вызова Транслатедиспатч

\[*Транслатедиспатч* доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен.\]

Используется клиентом функции [**дореадермоде**](doreadermode.md) для перехвата и явной обработки сообщений Windows, предназначенных для области прокрутки окна режима чтения. Это функция обратного вызова, определяемая приложением.

## <a name="syntax"></a>Синтаксис


```C++
BOOL CALLBACK TranslateDispatch(
  _In_ const MSG *lpmsg
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лпмсг* \[ окне\]
</dt> <dd>

Тип: **const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) \***

Указатель на структуру [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) , содержащую перехваченное сообщение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**

**Значение true** , если сообщение было обработано этой функцией; в противном случае — **значение false**. Если **значение равно false**, сообщение обрабатывается реализацией режима модуля чтения по умолчанию. Эта реализация обрабатывает перемещение и кнопки мыши, а также клавиши.

## <a name="examples"></a>Примеры

В следующем примере демонстрируется реализация этой функции.


```C++
BOOL CALLBACK
TranslateDispatchCallback(LPMSG lpmsg)
{
    BOOL fResult = FALSE;

    if (lpmsg->message == WM_KEYDOWN)
    {
        
        // Perform custom keyboard actions here.
        fResult = TRUE;
    }

    return fResult;
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows vista, только для \[ классических приложений Windows vista\]<br/> |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>          |



 

