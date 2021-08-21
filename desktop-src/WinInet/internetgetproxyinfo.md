---
title: Функция InternetGetProxyInfo
description: Получает данные прокси-сервера для доступа к указанным ресурсам.
ms.assetid: 5fc0f471-420c-4125-8323-cb1e1e72e43f
keywords:
- Функция Интернетжетпроксинфо WinINet
topic_type:
- apiref
api_name:
- InternetGetProxyInfo
api_location:
- JSProxy.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76965f63afb751e810daa6feffe76774f03daaaf7278996b4c6800f0efa42dfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113688"
---
# <a name="internetgetproxyinfo-function"></a>Функция InternetGetProxyInfo

> [!NOTE]
> Эта функция является устаревшей. Для поддержки автопрокси используйте вместо них службы HTTP (WinHTTP) версии 5,1. Дополнительные сведения см. в разделе [Поддержка автопрокси WinHTTP](../winhttp/winhttp-autoproxy-support.md).

Получает данные прокси-сервера для доступа к указанным ресурсам. Эту функцию можно вызвать только с помощью динамической привязки к "JSProxy.dll".

## <a name="syntax"></a>Синтаксис

```cpp
BOOL InternetGetProxyInfo(
  _In_  LPCSTR  lpszUrl,
  _In_  DWORD   dwUrlLength,
  _In_  LPSTR   lpszUrlHostName,
  _In_  DWORD   dwUrlHostNameLength,
  _Out_ LPSTR   *lplpszProxyHostName,
  _Out_ LPDWORD lpdwProxyHostNameLength
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*лпсзурл* \[ окне\]
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая указывает URL-адрес целевого ресурса HTTP.

</dd> <dt>

*двурлленгс* \[ окне\]
</dt> <dd>

Размер URL-адреса (в байтах), на который указывает *лпсзурл*.

</dd> <dt>

*лпсзурлхостнаме* \[ окне\]
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая указывает имя узла для целевого URL-адреса.

</dd> <dt>

*двурлхостнамеленгс* \[ окне\]
</dt> <dd>

Размер (в байтах) имени узла, на которое указывает *лпсзурлхостнаме*.

</dd> <dt>

*лплпсзпроксихостнаме* \[ заполняет\]
</dt> <dd>

Указатель на адрес буфера, который получает URL-адрес прокси для использования в HTTP-запросе для указанного ресурса. Приложение отвечает за освобождение этой строки.

</dd> <dt>

*лпдвпроксихостнамеленгс* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает размер строки в байтах, возвращаемой в буфере *лплпсзпроксихостнаме* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае. Чтобы получить расширенные данные об ошибках, вызовите [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarks

Чтобы вызвать **интернетжетпроксинфо**, необходимо динамически связать с ним, используя определенный тип указателя функции **пфнинтернетжетпроксинфо**. В следующем фрагменте кода показано, как объявить экземпляр этого типа указателя функции, а затем инициализировать и вызвать его.

```cpp
  HMODULE hModJS;                               // Handle for loading the DLL
  pfnInternetGetProxyInfo pIGPI;                // Function-pointer instance

  hModJS = LoadLibrary( TEXT("jsproxy.dll") );
  if (!hModJS)
  {
    _tprintf( TEXT("\nLoadLibrary failed to load jsproxy.dll with error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  pIGPI = (pfnInternetGetProxyInfo)
          GetProcAddress( hModJS, "InternetGetProxyInfo" );
  if (!pIGPI)         
  {
    _tprintf( TEXT("\nGetProcAddress failed to find InternetGetProxyInfo, error: %d\n"),
            GetLastError( ) );
    return( FALSE );
  }

  // The pIGPI function pointer can now be used to call InternetGetProxyInfo.
```

Как и все остальные аспекты API WinINet, эта функция не может быть безопасно вызвана из DllMain или конструкторов и деструкторов глобальных объектов.

> [!Note]  
> WinINet не поддерживает реализации серверов. Кроме того, его не следует использовать из службы. для серверных реализаций или служб используйте [Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>JSProxy.dll</dt> </dl> |

## <a name="see-also"></a>См. также

[**интернетинитиализеаутопроксидлл**](/windows/win32/api/winineti/nf-winineti-internetinitializeautoproxydll)

[**интернетдеинитиализеаутопроксидлл**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))

[**детектаутопроксюрл**](/windows/win32/api/winineti/nf-winineti-detectautoproxyurl)
