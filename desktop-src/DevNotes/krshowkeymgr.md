---
description: Открывает диалоговое окно диспетчера ключей в пользовательском интерфейсе.
ms.assetid: 65c2763f-42d5-4534-94f7-e753f6486014
title: Функция Кршовкэймгр
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KRShowKeyMgr
api_type:
- DllExport
api_location:
- Keymgr.dll
ms.openlocfilehash: 59b6b38cf7e78755c7d5c481a22a0a8b3854c8a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665159"
---
# <a name="krshowkeymgr-function"></a>Функция Кршовкэймгр

\[Эта функция включена только в Windows XP. В настоящее время она не включена ни в какую другую версию Windows, ни в одну из будущих версий Windows.\]

Открывает диалоговое окно диспетчера ключей в пользовательском интерфейсе.

## <a name="syntax"></a>Синтаксис


```C++
void KRShowKeyMgr(
   HWND      hwParent,
   HINSTANCE hInstance,
   LPWSTR    pszCmdLine,
   int       CmdShow
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хвпарент* 
</dt> <dd>

Маркер родительского окна диалога. Этот параметр может принимать значение **NULL**.

</dd> <dt>

*hInstance* 
</dt> <dd>

Этот параметр не используется и должен иметь значение **null**.

</dd> <dt>

*псзкмдлине* 
</dt> <dd>

Этот параметр не используется и должен иметь значение **null**.

</dd> <dt>

*кмдшов* 
</dt> <dd>

Этот параметр не используется и должен иметь значение **null**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Keymgr.dll</dt> </dl> |



 

 
