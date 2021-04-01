---
description: Регистрируется для уведомления при первой загрузке библиотеки DLL. Это уведомление происходит до того, как будет выполнена динамическая компоновка.
ms.assetid: c2757aa0-76fa-427a-a4f6-cb26e7f7d0d1
title: Функция Лдррегистердллнотификатион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrRegisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 82ec05a24f4cccc89cece666b18cb63412a78259
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072361"
---
# <a name="ldrregisterdllnotification-function"></a><span data-ttu-id="8e01b-104">Функция Лдррегистердллнотификатион</span><span class="sxs-lookup"><span data-stu-id="8e01b-104">LdrRegisterDllNotification function</span></span>

<span data-ttu-id="8e01b-105">\[Эта функция может быть изменена или удалена из Windows без предварительного уведомления.\]</span><span class="sxs-lookup"><span data-stu-id="8e01b-105">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="8e01b-106">Регистрируется для уведомления при первой загрузке библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="8e01b-106">Registers for notification when a DLL is first loaded.</span></span> <span data-ttu-id="8e01b-107">Это уведомление происходит до того, как будет выполнена динамическая компоновка.</span><span class="sxs-lookup"><span data-stu-id="8e01b-107">This notification occurs before dynamic linking takes place.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e01b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e01b-108">Syntax</span></span>


```C++
NTSTATUS NTAPI LdrRegisterDllNotification(
  _In_     ULONG                          Flags,
  _In_     PLDR_DLL_NOTIFICATION_FUNCTION NotificationFunction,
  _In_opt_ PVOID                          Context,
  _Out_    PVOID                          *Cookie
);
```



## <a name="parameters"></a><span data-ttu-id="8e01b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e01b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e01b-110">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e01b-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e01b-111">Этот параметр должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="8e01b-111">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8e01b-112">*Нотификатионфунктион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e01b-112">*NotificationFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e01b-113">Указатель на функцию обратного вызова уведомления [*лдрдллнотификатион*](ldrdllnotification.md) для вызова при загрузке библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="8e01b-113">A pointer to an [*LdrDllNotification*](ldrdllnotification.md) notification callback function to call when the DLL is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="8e01b-114">*Контекст* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8e01b-114">*Context* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8e01b-115">Указатель на данные контекста для функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="8e01b-115">A pointer to context data for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="8e01b-116">*Файл cookie* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8e01b-116">*Cookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e01b-117">Указатель на переменную, которая получает идентификатор для функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="8e01b-117">A pointer to a variable to receive an identifier for the callback function.</span></span> <span data-ttu-id="8e01b-118">Этот идентификатор используется для отмены регистрации функции обратного вызова уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8e01b-118">This identifier is used to unregister the notification callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e01b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e01b-119">Return value</span></span>

<span data-ttu-id="8e01b-120">Если функция завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="8e01b-120">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span>

<span data-ttu-id="8e01b-121">Формы и значения кодов ошибок **NTSTATUS** перечислены в файле заголовка NTSTATUS. h, доступном в WDK, и описаны в документации по WDK.</span><span class="sxs-lookup"><span data-stu-id="8e01b-121">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e01b-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e01b-122">Remarks</span></span>

<span data-ttu-id="8e01b-123">Эта функция не имеет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="8e01b-123">This function has no associated header file.</span></span> <span data-ttu-id="8e01b-124">Связанная библиотека импорта, NTDLL. lib, доступна в WDK.</span><span class="sxs-lookup"><span data-stu-id="8e01b-124">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="8e01b-125">Можно также использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="8e01b-125">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e01b-126">Требования</span><span class="sxs-lookup"><span data-stu-id="8e01b-126">Requirements</span></span>



| <span data-ttu-id="8e01b-127">Требование</span><span class="sxs-lookup"><span data-stu-id="8e01b-127">Requirement</span></span> | <span data-ttu-id="8e01b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="8e01b-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8e01b-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e01b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8e01b-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e01b-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8e01b-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e01b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8e01b-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8e01b-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8e01b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8e01b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e01b-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e01b-134"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e01b-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e01b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e01b-136">*лдрдллнотификатион*</span><span class="sxs-lookup"><span data-stu-id="8e01b-136">*LdrDllNotification*</span></span>](ldrdllnotification.md)
</dt> <dt>

[<span data-ttu-id="8e01b-137">**лдрунрегистердллнотификатион**</span><span class="sxs-lookup"><span data-stu-id="8e01b-137">**LdrUnregisterDllNotification**</span></span>](ldrunregisterdllnotification.md)
</dt> </dl>

 

 
