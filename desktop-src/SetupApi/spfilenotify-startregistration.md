---
description: При использовании директивы Регистердллс INF для самостоятельной регистрации библиотек DLL вызывающие объекты Сетупинсталлфроминфсектион могут получать уведомления о каждом файле при регистрации или отмене регистрации.
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: Сообщение SPFILENOTIFY_STARTREGISTRATION (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe795af38c21c17bf4e81692985d4bfe50dc8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664077"
---
# <a name="spfilenotify_startregistration-message"></a><span data-ttu-id="0ae3d-103">\_Сообщение спфиленотифи стартрегистратион</span><span class="sxs-lookup"><span data-stu-id="0ae3d-103">SPFILENOTIFY\_STARTREGISTRATION message</span></span>

<span data-ttu-id="0ae3d-104">При использовании директивы **регистердллс** INF для самостоятельной регистрации библиотек DLL вызывающие объекты [**сетупинсталлфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) могут получать уведомления о каждом файле при регистрации или отмене регистрации.</span><span class="sxs-lookup"><span data-stu-id="0ae3d-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="0ae3d-105">Чтобы отправить уведомление **спфиленотифи \_ стартрегистратион** в подпрограммы обратного вызова один раз перед регистрацией файла, включите \_ \_ в параметр " *flags* " в **сетупинсталлфроминфсектион**.</span><span class="sxs-lookup"><span data-stu-id="0ae3d-105">To send a **SPFILENOTIFY\_STARTREGISTRATION** notification to the callback routine once before registering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="0ae3d-106">Чтобы отправить уведомление об отмене регистрации, включите \_ регистеркаллбаккаваре и регуляторы \_ унрегсвр в параметре *flags* .</span><span class="sxs-lookup"><span data-stu-id="0ae3d-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="0ae3d-107">Подпрограммы обратного вызова, заданные параметром *мсгхандлер* параметра [**сетупинсталлфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) , должны быть [ \_ \_ обратным вызовом типа PSP File](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="0ae3d-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="0ae3d-108">Задайте для параметра *контекста* тот же *контекст* , который указан в **сетупинсталлфроминфсектион**.</span><span class="sxs-lookup"><span data-stu-id="0ae3d-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="0ae3d-109">Задайте для параметра *уведомления* значение **спфиленотифи \_ стартрегистратион**.</span><span class="sxs-lookup"><span data-stu-id="0ae3d-109">Set the *Notification* parameter to **SPFILENOTIFY\_STARTREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="0ae3d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ae3d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ae3d-111">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="0ae3d-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="0ae3d-112">Указатель на структуру [**\_ \_ \_ состояния управления регистром SP**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) , содержащую сведения о регистрируемом или незарегистрированном файле.</span><span class="sxs-lookup"><span data-stu-id="0ae3d-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="0ae3d-113">Элементу **кбсизе** должен быть присвоен размер структуры.</span><span class="sxs-lookup"><span data-stu-id="0ae3d-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="0ae3d-114">Элементу **filename** следует присвоить полный путь к регистрируемому файлу.</span><span class="sxs-lookup"><span data-stu-id="0ae3d-114">The **FileName** member should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="0ae3d-115">**Win32Error** не используется, и для него следует задать значение No \_ Error.</span><span class="sxs-lookup"><span data-stu-id="0ae3d-115">**Win32Error** is not used and should be set to NO\_ERROR.</span></span> <span data-ttu-id="0ae3d-116">**Фаилурекоде** не используется, и для него должно быть задано значение Спрег \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0ae3d-116">**FailureCode** is not used and should be set to SPREG\_SUCCESS.</span></span>

</dd> <dt>

<span data-ttu-id="0ae3d-117">*Param2*</span><span class="sxs-lookup"><span data-stu-id="0ae3d-117">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="0ae3d-118">Если файл регистрируется, для *Param2* должен быть задан указатель на ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="0ae3d-118">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="0ae3d-119">При отмене регистрации файла *Param2* должен быть установлен в указатель на нуль.</span><span class="sxs-lookup"><span data-stu-id="0ae3d-119">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ae3d-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ae3d-120">Return value</span></span>

<span data-ttu-id="0ae3d-121">После получения уведомления функция обратного вызова может вернуть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="0ae3d-121">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="0ae3d-122">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0ae3d-122">Return code</span></span>                                                                                  | <span data-ttu-id="0ae3d-123">Описание</span><span class="sxs-lookup"><span data-stu-id="0ae3d-123">Description</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ae3d-124"><dt>**прервать ФИЛЕОП \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0ae3d-124"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="0ae3d-125">Не регистрировать и не регистрировать файл, а также прерывать обработку раздела INF.</span><span class="sxs-lookup"><span data-stu-id="0ae3d-125">Do not register or unregister the file and stop processing the INF section.</span></span><br/>             |
| <dl> <span data-ttu-id="0ae3d-126"><dt>**ФИЛЕОП \_ доит**</dt></span><span class="sxs-lookup"><span data-stu-id="0ae3d-126"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="0ae3d-127">Зарегистрируйте или отмените регистрацию файла и продолжайте обработку раздела INF.</span><span class="sxs-lookup"><span data-stu-id="0ae3d-127">Register or unregister the file and continue processing the INF section.</span></span><br/>                |
| <dl> <span data-ttu-id="0ae3d-128"><dt>**\_Пропуск файла**</dt></span><span class="sxs-lookup"><span data-stu-id="0ae3d-128"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="0ae3d-129">Пропустить регистрацию или отменить регистрацию файла, но продолжить обработку раздела INF</span><span class="sxs-lookup"><span data-stu-id="0ae3d-129">Skip registration or unregistration of the file but continue processing the INF section</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0ae3d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="0ae3d-130">Requirements</span></span>



| <span data-ttu-id="0ae3d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="0ae3d-131">Requirement</span></span> | <span data-ttu-id="0ae3d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="0ae3d-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ae3d-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ae3d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0ae3d-134">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0ae3d-134">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0ae3d-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ae3d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0ae3d-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0ae3d-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ae3d-137">Header</span><span class="sxs-lookup"><span data-stu-id="0ae3d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ae3d-138"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ae3d-138"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ae3d-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ae3d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ae3d-140">Обзор</span><span class="sxs-lookup"><span data-stu-id="0ae3d-140">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="0ae3d-141">Уведомления</span><span class="sxs-lookup"><span data-stu-id="0ae3d-141">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="0ae3d-142">**сетупинсталлфроминфсектион**</span><span class="sxs-lookup"><span data-stu-id="0ae3d-142">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="0ae3d-143">**СПФИЛЕНОТИФИ \_ ендрегистратион**</span><span class="sxs-lookup"><span data-stu-id="0ae3d-143">**SPFILENOTIFY\_ENDREGISTRATION**</span></span>](spfilenotify-endregistration.md)
</dt> </dl>

 

