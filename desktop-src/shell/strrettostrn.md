---
description: 'Принимает структуру СТРРЕТ, возвращенную Ишеллфолдер:: Жетдисплайнамеоф, преобразует ее в строку и помещает результат в буфер.'
title: Функция Стрреттострн
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrRetToStrN
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: a816fb5f-8320-4b63-a85d-dd4c59596ead
ms.openlocfilehash: 89a8d991e22e8615456bd8d4690c046ec0d325d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997954"
---
# <a name="strrettostrn-function"></a>Функция Стрреттострн

Принимает структуру [**стррет**](/windows/desktop/api/Shtypes/ns-shtypes-strret) , возвращенную [**Ишеллфолдер:: жетдисплайнамеоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), преобразует ее в строку и помещает результат в буфер.

## <a name="syntax"></a>Синтаксис


```C++
BOOL StrRetToStrN(
  _Out_   LPTSTR        pszOut,
  _In_    UINT          cchOut,
  _Inout_ LPSTRRET      pStrRet,
  _In_    LPCITEMIDLIST pidl
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псзаут* \[ заполняет\]
</dt> <dd>

Тип: **LPTSTR**

Буфер для хранения отображаемого имени. Он будет возвращен в виде строки, завершающейся нулем. Если *кчаут* слишком мал, имя будет обрезано до размера.

</dd> <dt>

*кчаут* \[ окне\]
</dt> <dd>

Тип: **uint**

Размер *псзаут* в символах. Если *кчаут* слишком мал, строка будет обрезана до размера.

</dd> <dt>

*пстррет* \[ в, out\]
</dt> <dd>

Тип: **лпстррет**

Указатель на структуру [**стррет**](/windows/desktop/api/Shtypes/ns-shtypes-strret) . Когда функция возвращает, этот указатель больше не будет действительным.

</dd> <dt>

*Пидл* \[ окне\]
</dt> <dd>

Тип: **лпЦитемидлист**

Указатель на структуру [**итемидлист**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) элемента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **bool** .

**True** для успешного выполнения, **false** для сбоя.

## <a name="remarks"></a>Примечания

> [!Note]  
> Начиная с версии Shell32.dll 5,0, вызов этой функции эквивалентен вызову [**стрреттобуф**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).

 

**Стрреттострн** не экспортируется по имени. Чтобы использовать его, необходимо использовать [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) и запросить порядковый номер 96 из Shell32.dll для получения указателя на функцию.

Если элемент **утипе** структуры, на который указывает *пстррет* , имеет значение **Стррет \_ встр**, то элемент **полестр** этой структуры будет освобожден при возврате.

Обратите внимание, что эта функция экспортируется из Shell32.dll, а не Shlwapi.dll. Он также включается в Шлобж. h, а не в Shlwapi. h.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**стрреттостр**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[**стрреттобуф**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
