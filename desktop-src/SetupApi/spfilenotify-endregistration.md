---
description: При использовании директивы Регистердллс INF для самостоятельной регистрации библиотек DLL вызывающие объекты Сетупинсталлфроминфсектион могут получать уведомления о каждом файле при регистрации или отмене регистрации.
ms.assetid: 6304f406-c9f8-41cc-a7b7-5ef606f62efb
title: Сообщение SPFILENOTIFY_ENDREGISTRATION (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8992d318d605110d74521efdb8a9c911aeeb9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664527"
---
# <a name="spfilenotify_endregistration-message"></a><span data-ttu-id="c8d15-103">\_Сообщение спфиленотифи ендрегистратион</span><span class="sxs-lookup"><span data-stu-id="c8d15-103">SPFILENOTIFY\_ENDREGISTRATION message</span></span>

<span data-ttu-id="c8d15-104">При использовании директивы **регистердллс** INF для самостоятельной регистрации библиотек DLL вызывающие объекты [**сетупинсталлфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) могут получать уведомления о каждом файле при регистрации или отмене регистрации.</span><span class="sxs-lookup"><span data-stu-id="c8d15-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="c8d15-105">Чтобы отправить **спфиленотифи \_ ендрегистратион** уведомление в подпрограммы обратного вызова после регистрации или отмены регистрации файла, включите \_ \_ в параметр *flags* в **сетупинсталлфроминфсектион** значение Spin регистеркаллбаккаваре и Spin регсвр.</span><span class="sxs-lookup"><span data-stu-id="c8d15-105">To send a **SPFILENOTIFY\_ENDREGISTRATION** notification to a callback routine once after registering or unregistering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="c8d15-106">Чтобы отправить уведомление об отмене регистрации, включите \_ регистеркаллбаккаваре и регуляторы \_ унрегсвр в параметре *flags* .</span><span class="sxs-lookup"><span data-stu-id="c8d15-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="c8d15-107">Подпрограммы обратного вызова, заданные параметром *мсгхандлер* параметра [**сетупинсталлфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) , должны быть [ \_ \_ обратным вызовом типа PSP File](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="c8d15-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="c8d15-108">Задайте для параметра *контекста* тот же *контекст* , который указан в **сетупинсталлфроминфсектион**.</span><span class="sxs-lookup"><span data-stu-id="c8d15-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="c8d15-109">Задайте для параметра *уведомления* значение **спфиленотифи \_ ендрегистратион**.</span><span class="sxs-lookup"><span data-stu-id="c8d15-109">Set the *Notification* parameter to **SPFILENOTIFY\_ENDREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_ENDREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="c8d15-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8d15-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8d15-111">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="c8d15-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="c8d15-112">Указатель на структуру [**\_ \_ \_ состояния управления регистром SP**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) , содержащую сведения о регистрируемом или незарегистрированном файле.</span><span class="sxs-lookup"><span data-stu-id="c8d15-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="c8d15-113">Элементу **кбсизе** должен быть присвоен размер структуры.</span><span class="sxs-lookup"><span data-stu-id="c8d15-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="c8d15-114">Для **filename** необходимо указать полный путь к регистрируемому файлу.</span><span class="sxs-lookup"><span data-stu-id="c8d15-114">**FileName** should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="c8d15-115">Для **Win32Error** должен быть задан [код системной ошибки](/windows/desktop/Debug/system-error-codes) , указывающий код расширенной ошибки.</span><span class="sxs-lookup"><span data-stu-id="c8d15-115">**Win32Error** should be set to a [system error code](/windows/desktop/Debug/system-error-codes) indicating an extended error code.</span></span> <span data-ttu-id="c8d15-116">Для **фаилурекоде** следует задать один из допустимых кодов сбоя, указывающий результат регистрации.</span><span class="sxs-lookup"><span data-stu-id="c8d15-116">**FailureCode** should be set to one of the valid failure codes indicating the outcome of the registration.</span></span> <span data-ttu-id="c8d15-117">Допустимые коды ошибок см. в разделе [**\_ \_ \_ состояние управления регистром SP**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).</span><span class="sxs-lookup"><span data-stu-id="c8d15-117">For valid failure codes see [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).</span></span>

</dd> <dt>

<span data-ttu-id="c8d15-118">*Param2*</span><span class="sxs-lookup"><span data-stu-id="c8d15-118">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="c8d15-119">Если файл регистрируется, для *Param2* должен быть задан указатель на ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="c8d15-119">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="c8d15-120">При отмене регистрации файла *Param2* должен быть установлен в указатель на нуль.</span><span class="sxs-lookup"><span data-stu-id="c8d15-120">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8d15-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8d15-121">Return value</span></span>

<span data-ttu-id="c8d15-122">После получения уведомления функция обратного вызова может вернуть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c8d15-122">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="c8d15-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c8d15-123">Return code</span></span>                                                                                  | <span data-ttu-id="c8d15-124">Описание</span><span class="sxs-lookup"><span data-stu-id="c8d15-124">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="c8d15-125"><dt>**прервать ФИЛЕОП \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c8d15-125"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="c8d15-126">Прерывать обработку раздела INF.</span><span class="sxs-lookup"><span data-stu-id="c8d15-126">Stop processing the INF section.</span></span><br/>     |
| <dl> <span data-ttu-id="c8d15-127"><dt>**ФИЛЕОП \_ доит**</dt></span><span class="sxs-lookup"><span data-stu-id="c8d15-127"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="c8d15-128">Продолжить обработку раздела INF.</span><span class="sxs-lookup"><span data-stu-id="c8d15-128">Continue processing the INF section.</span></span><br/> |
| <dl> <span data-ttu-id="c8d15-129"><dt>**\_Пропуск файла**</dt></span><span class="sxs-lookup"><span data-stu-id="c8d15-129"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="c8d15-130">Продолжить обработку раздела INF</span><span class="sxs-lookup"><span data-stu-id="c8d15-130">Continue processing the INF section</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="c8d15-131">Требования</span><span class="sxs-lookup"><span data-stu-id="c8d15-131">Requirements</span></span>



| <span data-ttu-id="c8d15-132">Требование</span><span class="sxs-lookup"><span data-stu-id="c8d15-132">Requirement</span></span> | <span data-ttu-id="c8d15-133">Значение</span><span class="sxs-lookup"><span data-stu-id="c8d15-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8d15-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8d15-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c8d15-135">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c8d15-135">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c8d15-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8d15-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c8d15-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c8d15-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8d15-138">Header</span><span class="sxs-lookup"><span data-stu-id="c8d15-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8d15-139"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8d15-139"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8d15-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8d15-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8d15-141">Обзор</span><span class="sxs-lookup"><span data-stu-id="c8d15-141">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="c8d15-142">Уведомления</span><span class="sxs-lookup"><span data-stu-id="c8d15-142">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="c8d15-143">**сетупинсталлфроминфсектион**</span><span class="sxs-lookup"><span data-stu-id="c8d15-143">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="c8d15-144">**СПФИЛЕНОТИФИ \_ стартрегистратион**</span><span class="sxs-lookup"><span data-stu-id="c8d15-144">**SPFILENOTIFY\_STARTREGISTRATION**</span></span>](spfilenotify-startregistration.md)
</dt> </dl>

 

