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
ms.openlocfilehash: ef441754fd5de09e3792d9269f05d96ecc08aa23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415564"
---
# <a name="internetgetproxyinfo-function"></a><span data-ttu-id="e188b-104">Функция InternetGetProxyInfo</span><span class="sxs-lookup"><span data-stu-id="e188b-104">InternetGetProxyInfo function</span></span>

> [!NOTE]
> <span data-ttu-id="e188b-105">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="e188b-105">This function is deprecated.</span></span> <span data-ttu-id="e188b-106">Для поддержки автопрокси используйте вместо них службы HTTP (WinHTTP) версии 5,1.</span><span class="sxs-lookup"><span data-stu-id="e188b-106">For autoproxy support, use HTTP Services (WinHTTP) version 5.1 instead.</span></span> <span data-ttu-id="e188b-107">Дополнительные сведения см. в разделе [Поддержка автопрокси WinHTTP](../winhttp/winhttp-autoproxy-support.md).</span><span class="sxs-lookup"><span data-stu-id="e188b-107">For more information, see [WinHTTP AutoProxy Support](../winhttp/winhttp-autoproxy-support.md).</span></span>

<span data-ttu-id="e188b-108">Получает данные прокси-сервера для доступа к указанным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="e188b-108">Retrieves proxy data for accessing specified resources.</span></span> <span data-ttu-id="e188b-109">Эту функцию можно вызвать только с помощью динамической привязки к "JSProxy.dll".</span><span class="sxs-lookup"><span data-stu-id="e188b-109">This function can only be called by dynamically linking to "JSProxy.dll".</span></span>

## <a name="syntax"></a><span data-ttu-id="e188b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e188b-110">Syntax</span></span>

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

## <a name="parameters"></a><span data-ttu-id="e188b-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e188b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e188b-112">*лпсзурл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e188b-112">*lpszUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e188b-113">Указатель на строку, завершающуюся нулем, которая указывает URL-адрес целевого ресурса HTTP.</span><span class="sxs-lookup"><span data-stu-id="e188b-113">A pointer to a null-terminated string that specifies the URL of the target HTTP resource.</span></span>

</dd> <dt>

<span data-ttu-id="e188b-114">*двурлленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e188b-114">*dwUrlLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e188b-115">Размер URL-адреса (в байтах), на который указывает *лпсзурл*.</span><span class="sxs-lookup"><span data-stu-id="e188b-115">The size, in bytes, of the URL pointed to by *lpszUrl*.</span></span>

</dd> <dt>

<span data-ttu-id="e188b-116">*лпсзурлхостнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e188b-116">*lpszUrlHostName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e188b-117">Указатель на строку, завершающуюся нулем, которая указывает имя узла для целевого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="e188b-117">A pointer to a null-terminated string that specifies the host name of the target URL.</span></span>

</dd> <dt>

<span data-ttu-id="e188b-118">*двурлхостнамеленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e188b-118">*dwUrlHostNameLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e188b-119">Размер (в байтах) имени узла, на которое указывает *лпсзурлхостнаме*.</span><span class="sxs-lookup"><span data-stu-id="e188b-119">The size, in bytes, of the host name pointed to by *lpszUrlHostName*.</span></span>

</dd> <dt>

<span data-ttu-id="e188b-120">*лплпсзпроксихостнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e188b-120">*lplpszProxyHostName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e188b-121">Указатель на адрес буфера, который получает URL-адрес прокси для использования в HTTP-запросе для указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="e188b-121">A pointer to the address of a buffer that receives the URL of the proxy to use in an HTTP request for the specified resource.</span></span> <span data-ttu-id="e188b-122">Приложение отвечает за освобождение этой строки.</span><span class="sxs-lookup"><span data-stu-id="e188b-122">The application is responsible for freeing this string.</span></span>

</dd> <dt>

<span data-ttu-id="e188b-123">*лпдвпроксихостнамеленгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e188b-123">*lpdwProxyHostNameLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e188b-124">Указатель на переменную, которая получает размер строки в байтах, возвращаемой в буфере *лплпсзпроксихостнаме* .</span><span class="sxs-lookup"><span data-stu-id="e188b-124">A pointer to a variable that receives the size, in bytes, of the string returned in the *lplpszProxyHostName* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e188b-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e188b-125">Return value</span></span>

<span data-ttu-id="e188b-126">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e188b-126">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="e188b-127">Чтобы получить расширенные данные об ошибках, вызовите [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="e188b-127">To get extended error data, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="e188b-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e188b-128">Remarks</span></span>

<span data-ttu-id="e188b-129">Чтобы вызвать **интернетжетпроксинфо**, необходимо динамически связать с ним, используя определенный тип указателя функции **пфнинтернетжетпроксинфо**.</span><span class="sxs-lookup"><span data-stu-id="e188b-129">To call **InternetGetProxyInfo**, you must dynamically link to it using the defined function-pointer type **pfnInternetGetProxyInfo**.</span></span> <span data-ttu-id="e188b-130">В следующем фрагменте кода показано, как объявить экземпляр этого типа указателя функции, а затем инициализировать и вызвать его.</span><span class="sxs-lookup"><span data-stu-id="e188b-130">The code snippet below shows how to declare an instance of this function-pointer type and then initialize and call it.</span></span>

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

<span data-ttu-id="e188b-131">Как и все остальные аспекты API WinINet, эта функция не может быть безопасно вызвана из DllMain или конструкторов и деструкторов глобальных объектов.</span><span class="sxs-lookup"><span data-stu-id="e188b-131">Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.</span></span>

> [!Note]  
> <span data-ttu-id="e188b-132">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="e188b-132">WinINet does not support server implementations.</span></span> <span data-ttu-id="e188b-133">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="e188b-133">In addition, it should not be used from a service.</span></span> <span data-ttu-id="e188b-134">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="e188b-134">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

## <a name="requirements"></a><span data-ttu-id="e188b-135">Требования</span><span class="sxs-lookup"><span data-stu-id="e188b-135">Requirements</span></span>

| <span data-ttu-id="e188b-136">Требование</span><span class="sxs-lookup"><span data-stu-id="e188b-136">Requirement</span></span> | <span data-ttu-id="e188b-137">Значение</span><span class="sxs-lookup"><span data-stu-id="e188b-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e188b-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e188b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e188b-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e188b-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e188b-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e188b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e188b-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e188b-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e188b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e188b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e188b-143"><dt>JSProxy.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e188b-143"><dt>JSProxy.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="e188b-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e188b-144">See also</span></span>

[<span data-ttu-id="e188b-145">**интернетинитиализеаутопроксидлл**</span><span class="sxs-lookup"><span data-stu-id="e188b-145">**InternetInitializeAutoProxyDll**</span></span>](/windows/win32/api/winineti/nf-winineti-internetinitializeautoproxydll)

<span data-ttu-id="e188b-146">[**интернетдеинитиализеаутопроксидлл**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e188b-146">[**InternetDeInitializeAutoProxyDll**](/previous-versions/windows/desktop/legacy/aa384580(v=vs.85))</span></span>

[<span data-ttu-id="e188b-147">**детектаутопроксюрл**</span><span class="sxs-lookup"><span data-stu-id="e188b-147">**DetectAutoProxyUrl**</span></span>](/windows/win32/api/winineti/nf-winineti-detectautoproxyurl)
