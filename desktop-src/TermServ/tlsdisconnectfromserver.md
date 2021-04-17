---
title: Функция Тлсдисконнектфромсервер
description: Закрывает открытый маркер для сервера лицензий удаленный рабочий стол.
ms.assetid: b4b001ec-823b-4514-bbec-839a83a9a189
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов функции Тлсдисконнектфромсервер
topic_type:
- apiref
api_name:
- TLSDisconnectFromServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 265a6b04186bd640943cf2b348dda7afcf8f712a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682110"
---
# <a name="tlsdisconnectfromserver-function"></a><span data-ttu-id="da28f-104">Функция Тлсдисконнектфромсервер</span><span class="sxs-lookup"><span data-stu-id="da28f-104">TLSDisconnectFromServer function</span></span>

<span data-ttu-id="da28f-105">Закрывает открытый маркер для сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="da28f-105">Closes an open handle to a Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="da28f-106">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="da28f-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="da28f-107">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="da28f-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="da28f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da28f-108">Syntax</span></span>


```C++
void WINAPI TLSDisconnectFromServer(
  _In_ TLS_HANDLE hHandle
);
```



## <a name="parameters"></a><span data-ttu-id="da28f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="da28f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da28f-110">*ххандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da28f-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da28f-111">Обработчик на удаленный рабочий стол сервере лицензирования, который открыт при вызове функции [**тлсконнекттолссервер**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="da28f-111">Handle to a Remote Desktop license server that is opened by a call to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da28f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da28f-112">Return value</span></span>

<span data-ttu-id="da28f-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="da28f-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da28f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da28f-114">Remarks</span></span>

<span data-ttu-id="da28f-115">Вызовите функцию **тлсдисконнектфромсервер** в рамках программы очистки программы, чтобы закрыть все дескрипторы сервера, открытые с помощью вызовов функции [**тлсконнекттолссервер**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="da28f-115">Call the **TLSDisconnectFromServer** function as part of your program's clean-up routine to close all the server handles that are opened by calls to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="da28f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="da28f-116">Requirements</span></span>



| <span data-ttu-id="da28f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="da28f-117">Requirement</span></span> | <span data-ttu-id="da28f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="da28f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da28f-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da28f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="da28f-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da28f-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da28f-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da28f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="da28f-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da28f-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da28f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="da28f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da28f-124"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da28f-124"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da28f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da28f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da28f-126">**\_маркер TLS**</span><span class="sxs-lookup"><span data-stu-id="da28f-126">**TLS\_HANDLE**</span></span>](tls-handle.md)
</dt> <dt>

[<span data-ttu-id="da28f-127">**тлсконнекттолссервер**</span><span class="sxs-lookup"><span data-stu-id="da28f-127">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> </dl>

 

