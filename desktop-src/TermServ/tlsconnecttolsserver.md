---
title: Функция Тлсконнекттолссервер
description: Открывает маркер указанного сервера лицензий удаленный рабочий стол.
ms.assetid: 9e90a8e8-9319-42ee-b541-a1d028b6ed4d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов функции Тлсконнекттолссервер
topic_type:
- apiref
api_name:
- TLSConnectToLsServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7f36b519399f0a8c1627fad7c7768f36ece57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415740"
---
# <a name="tlsconnecttolsserver-function"></a><span data-ttu-id="64b78-104">Функция Тлсконнекттолссервер</span><span class="sxs-lookup"><span data-stu-id="64b78-104">TLSConnectToLsServer function</span></span>

<span data-ttu-id="64b78-105">Открывает маркер указанного сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="64b78-105">Opens a handle to the specified Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="64b78-106">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="64b78-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="64b78-107">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="64b78-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="64b78-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64b78-108">Syntax</span></span>


```C++
TLS_HANDLE WINAPI TLSConnectToLsServer(
  _In_ LPTSTR pszLsServer
);
```



## <a name="parameters"></a><span data-ttu-id="64b78-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="64b78-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64b78-110">*псзлссервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64b78-110">*pszLsServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64b78-111">Указатель на строку, завершающуюся **нулем**, которая указывает NetBIOS-имя сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="64b78-111">Pointer to a **null**-terminated string that specifies the NetBIOS name of the Remote Desktop license server.</span></span> <span data-ttu-id="64b78-112">Если значение этого параметра равно **null**, то указанный сервер является локальным компьютером.</span><span class="sxs-lookup"><span data-stu-id="64b78-112">If the value of this parameter is **NULL**, the specified server is the local computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64b78-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64b78-113">Return value</span></span>

<span data-ttu-id="64b78-114">Если функция выполнена, возвращаемое значение является обработчиком указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="64b78-114">If the function succeeds, the return value is a handle to the specified server.</span></span>

<span data-ttu-id="64b78-115">Если функция завершается ошибкой, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="64b78-115">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="64b78-116">Чтобы получить расширенные сведения об ошибке, вызовите функцию [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="64b78-116">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="64b78-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64b78-117">Remarks</span></span>

<span data-ttu-id="64b78-118">После завершения использования маркера, возвращаемого функцией **тлсконнекттолссервер** , выпустите его, вызвав функцию [**тлсдисконнектфромсервер**](tlsdisconnectfromserver.md) .</span><span class="sxs-lookup"><span data-stu-id="64b78-118">When you have finished using the handle that is returned by the **TLSConnectToLsServer** function, release it by calling the [**TLSDisconnectFromServer**](tlsdisconnectfromserver.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="64b78-119">Требования</span><span class="sxs-lookup"><span data-stu-id="64b78-119">Requirements</span></span>



| <span data-ttu-id="64b78-120">Требование</span><span class="sxs-lookup"><span data-stu-id="64b78-120">Requirement</span></span> | <span data-ttu-id="64b78-121">Значение</span><span class="sxs-lookup"><span data-stu-id="64b78-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64b78-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64b78-122">Minimum supported client</span></span><br/> | <span data-ttu-id="64b78-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64b78-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64b78-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64b78-124">Minimum supported server</span></span><br/> | <span data-ttu-id="64b78-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64b78-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64b78-126">DLL</span><span class="sxs-lookup"><span data-stu-id="64b78-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64b78-127"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64b78-127"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64b78-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64b78-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64b78-129">**\_маркер TLS**</span><span class="sxs-lookup"><span data-stu-id="64b78-129">**TLS\_HANDLE**</span></span>](tls-handle.md)
</dt> <dt>

[<span data-ttu-id="64b78-130">**тлсдисконнектфромсервер**</span><span class="sxs-lookup"><span data-stu-id="64b78-130">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> </dl>

 

