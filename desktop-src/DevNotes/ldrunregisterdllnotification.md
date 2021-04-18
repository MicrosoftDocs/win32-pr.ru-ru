---
description: Отменяет уведомление о загрузке DLL, зарегистрированное ранее путем вызова функции Лдррегистердллнотификатион.
ms.assetid: 18c3a027-e3cb-4083-afdc-00f416a70d8c
title: Функция Лдрунрегистердллнотификатион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrUnregisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 1fee03b4a06d274b495070eb40833b270a795158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423190"
---
# <a name="ldrunregisterdllnotification-function"></a><span data-ttu-id="c9df2-103">Функция Лдрунрегистердллнотификатион</span><span class="sxs-lookup"><span data-stu-id="c9df2-103">LdrUnregisterDllNotification function</span></span>

<span data-ttu-id="c9df2-104">\[Эта функция может быть изменена или удалена из Windows без предварительного уведомления.\]</span><span class="sxs-lookup"><span data-stu-id="c9df2-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="c9df2-105">Отменяет уведомление о загрузке DLL, зарегистрированное ранее путем вызова функции [**лдррегистердллнотификатион**](ldrregisterdllnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="c9df2-105">Cancels DLL load notification previously registered by calling the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9df2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9df2-106">Syntax</span></span>


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a><span data-ttu-id="c9df2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9df2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9df2-108">*Файл cookie* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c9df2-108">*Cookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9df2-109">Указатель на идентификатор обратного вызова, полученный из вызова [**лдррегистердллнотификатион**](ldrregisterdllnotification.md) , зарегистрированного для уведомления.</span><span class="sxs-lookup"><span data-stu-id="c9df2-109">A pointer to the callback identifier received from the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) call that registered for notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9df2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9df2-110">Return value</span></span>

<span data-ttu-id="c9df2-111">Возвращает код **NTSTATUS** или ошибки.</span><span class="sxs-lookup"><span data-stu-id="c9df2-111">Returns an **NTSTATUS** or error code.</span></span>

<span data-ttu-id="c9df2-112">Если функция завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="c9df2-112">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span>

<span data-ttu-id="c9df2-113">Если функция обратного вызова не найдена, функция возвращает **\_ библиотеку DLL состояния \_ не \_ найдена**.</span><span class="sxs-lookup"><span data-stu-id="c9df2-113">If the callback function is not found, the function returns **STATUS\_DLL\_NOT\_FOUND**.</span></span>

<span data-ttu-id="c9df2-114">Формы и значения кодов ошибок **NTSTATUS** перечислены в файле заголовка NTSTATUS. h, доступном в WDK, и описаны в документации по WDK.</span><span class="sxs-lookup"><span data-stu-id="c9df2-114">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9df2-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9df2-115">Remarks</span></span>

<span data-ttu-id="c9df2-116">Эта функция не имеет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="c9df2-116">This function has no associated header file.</span></span> <span data-ttu-id="c9df2-117">Связанная библиотека импорта, NTDLL. lib, доступна в WDK.</span><span class="sxs-lookup"><span data-stu-id="c9df2-117">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="c9df2-118">Можно также использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="c9df2-118">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9df2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c9df2-119">Requirements</span></span>



| <span data-ttu-id="c9df2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c9df2-120">Requirement</span></span> | <span data-ttu-id="c9df2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c9df2-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c9df2-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9df2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c9df2-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9df2-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c9df2-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9df2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c9df2-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c9df2-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c9df2-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c9df2-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9df2-127"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9df2-127"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9df2-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9df2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9df2-129">**лдррегистердллнотификатион**</span><span class="sxs-lookup"><span data-stu-id="c9df2-129">**LdrRegisterDllNotification**</span></span>](ldrregisterdllnotification.md)
</dt> </dl>

 

 
