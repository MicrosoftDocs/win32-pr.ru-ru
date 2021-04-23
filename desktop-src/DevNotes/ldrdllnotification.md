---
description: Функция обратного вызова уведомлений, указанная с помощью функции Лдррегистердллнотификатион.
ms.assetid: 12202797-c80c-4fa3-9cc4-dcb1a9f01551
title: Функция обратного вызова Лдрдллнотификатион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrDllNotification
- PLDR_DLL_NOTIFICATION_FUNCTION
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e29cd7b17c634250f56cbafcf86379449ac88199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895342"
---
# <a name="ldrdllnotification-callback-function"></a><span data-ttu-id="a4bcd-103">Функция обратного вызова Лдрдллнотификатион</span><span class="sxs-lookup"><span data-stu-id="a4bcd-103">LdrDllNotification callback function</span></span>

<span data-ttu-id="a4bcd-104">\[Эта функция может быть изменена или удалена из Windows без предварительного уведомления.\]</span><span class="sxs-lookup"><span data-stu-id="a4bcd-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="a4bcd-105">Функция обратного вызова уведомлений, указанная с помощью функции [**лдррегистердллнотификатион**](ldrregisterdllnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="a4bcd-105">A notification callback function specified with the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) function.</span></span> <span data-ttu-id="a4bcd-106">Загрузчик вызывает эту функцию при первой загрузке библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="a4bcd-106">The loader calls this function when a DLL is first loaded.</span></span>

<span data-ttu-id="a4bcd-107">**Предупреждение:** Функция обратного вызова уведомлений не является опасной для вызова функций в любой библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="a4bcd-107">**Warning:** It is unsafe for the notification callback function to call functions in any DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4bcd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4bcd-108">Syntax</span></span>


```C++
VOID CALLBACK LdrDllNotification(
  _In_     ULONG                       NotificationReason,
  _In_     PCLDR_DLL_NOTIFICATION_DATA NotificationData,
  _In_opt_ PVOID                       Context
);
```



## <a name="parameters"></a><span data-ttu-id="a4bcd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4bcd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4bcd-110">*Нотификатионреасон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4bcd-110">*NotificationReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4bcd-111">Причина, по которой была вызвана функция обратного вызова уведомлений.</span><span class="sxs-lookup"><span data-stu-id="a4bcd-111">The reason that the notification callback function was called.</span></span> <span data-ttu-id="a4bcd-112">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="a4bcd-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a4bcd-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a4bcd-113">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="a4bcd-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a4bcd-114">Meaning</span></span>                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <span data-ttu-id="a4bcd-115"><dt>**LDR \_ \_Причина уведомления библиотеки DLL \_ \_ загружена**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a4bcd-115"><dt>**LDR\_DLL\_NOTIFICATION\_REASON\_LOADED**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="a4bcd-116">Библиотека DLL загружена.</span><span class="sxs-lookup"><span data-stu-id="a4bcd-116">The DLL was loaded.</span></span> <span data-ttu-id="a4bcd-117">Параметр *нотификатиондата* указывает на структуру **\_ \_ \_ \_ данных уведомления загруженной библиотеки DLL LDR** .</span><span class="sxs-lookup"><span data-stu-id="a4bcd-117">The *NotificationData* parameter points to an **LDR\_DLL\_LOADED\_NOTIFICATION\_DATA** structure.</span></span> <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <span data-ttu-id="a4bcd-118"><dt>**LDR \_ \_Причина уведомления \_ DLL \_ выгружена**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a4bcd-118"><dt>**LDR\_DLL\_NOTIFICATION\_REASON\_UNLOADED**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="a4bcd-119">Библиотека DLL выгружена.</span><span class="sxs-lookup"><span data-stu-id="a4bcd-119">The DLL was unloaded.</span></span> <span data-ttu-id="a4bcd-120">Параметр *нотификатиондата* указывает на структуру **\_ \_ \_ \_ данных невыгруженных уведомлений библиотеки DLL LDR** .</span><span class="sxs-lookup"><span data-stu-id="a4bcd-120">The *NotificationData* parameter points to an **LDR\_DLL\_UNLOADED\_NOTIFICATION\_DATA** structure.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="a4bcd-121">*Нотификатиондата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4bcd-121">*NotificationData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4bcd-122">Указатель на постоянное объединение **уведомлений LDR \_ DLL \_** , которое содержит данные уведомления.</span><span class="sxs-lookup"><span data-stu-id="a4bcd-122">A pointer to a constant **LDR\_DLL\_NOTIFICATION** union that contains notification data.</span></span> <span data-ttu-id="a4bcd-123">Это объединение имеет следующее определение:</span><span class="sxs-lookup"><span data-stu-id="a4bcd-123">This union has the following definition:</span></span>

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

<span data-ttu-id="a4bcd-124">Структура **\_ \_ \_ \_ данных уведомления загруженной библиотеки DLL LDR** имеет следующее определение:</span><span class="sxs-lookup"><span data-stu-id="a4bcd-124">The **LDR\_DLL\_LOADED\_NOTIFICATION\_DATA** structure has the following definition:</span></span>

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

<span data-ttu-id="a4bcd-125">Структура **\_ \_ \_ \_ данных уведомления для выгруженной DLL-библиотеки LDR** имеет следующее определение:</span><span class="sxs-lookup"><span data-stu-id="a4bcd-125">The **LDR\_DLL\_UNLOADED\_NOTIFICATION\_DATA** structure has the following definition:</span></span>

``` syntax
typedef struct _LDR_DLL_UNLOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_UNLOADED_NOTIFICATION_DATA, *PLDR_DLL_UNLOADED_NOTIFICATION_DATA;
```

</dd> <dt>

<span data-ttu-id="a4bcd-126">*Контекст* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="a4bcd-126">*Context* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a4bcd-127">Указатель на данные контекста для функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="a4bcd-127">A pointer to context data for the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4bcd-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4bcd-128">Return value</span></span>

<span data-ttu-id="a4bcd-129">Эта функция обратного вызова не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a4bcd-129">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4bcd-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4bcd-130">Remarks</span></span>

<span data-ttu-id="a4bcd-131">Функция обратного вызова уведомлений вызывается до того, как будет выполнена динамическая компоновка.</span><span class="sxs-lookup"><span data-stu-id="a4bcd-131">The notification callback function is called before dynamic linking takes place.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4bcd-132">Требования</span><span class="sxs-lookup"><span data-stu-id="a4bcd-132">Requirements</span></span>



| <span data-ttu-id="a4bcd-133">Требование</span><span class="sxs-lookup"><span data-stu-id="a4bcd-133">Requirement</span></span> | <span data-ttu-id="a4bcd-134">Значение</span><span class="sxs-lookup"><span data-stu-id="a4bcd-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a4bcd-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4bcd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a4bcd-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4bcd-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a4bcd-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4bcd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a4bcd-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a4bcd-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a4bcd-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4bcd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4bcd-140">**лдррегистердллнотификатион**</span><span class="sxs-lookup"><span data-stu-id="a4bcd-140">**LdrRegisterDllNotification**</span></span>](ldrregisterdllnotification.md)
</dt> <dt>

[<span data-ttu-id="a4bcd-141">**лдрунрегистердллнотификатион**</span><span class="sxs-lookup"><span data-stu-id="a4bcd-141">**LdrUnregisterDllNotification**</span></span>](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




