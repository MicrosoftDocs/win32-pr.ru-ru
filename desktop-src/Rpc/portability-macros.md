---
title: Переносимые макросы (RPC. h)
description: Средства удаленного вызова процедур обеспечивают модель, вызов и независимость от соглашений об именовании путем связывания типов данных и типов, возвращаемых функцией, в созданных файлах-заглушках и файлах заголовков с определениями, характерными для каждой платформы.
ms.assetid: 94de1138-5a84-41d8-bf88-97f0ac630f5f
keywords:
- УДАЛЕНная совместимость макросов
topic_type:
- apiref
api_name:
- Portability Macros
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c184365496db7757524a12f1b0807c3c53e24b27
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "103999843"
---
# <a name="portability-macros"></a><span data-ttu-id="c67a6-104">Переносимые макросы</span><span class="sxs-lookup"><span data-stu-id="c67a6-104">Portability Macros</span></span>

<span data-ttu-id="c67a6-105">Средства удаленного вызова процедур обеспечивают модель, вызов и независимость от соглашений об именовании путем связывания типов данных и типов, возвращаемых функцией, в созданных файлах-заглушках и файлах заголовков с определениями, характерными для каждой платформы.</span><span class="sxs-lookup"><span data-stu-id="c67a6-105">The RPC tools achieve model, calling, and naming-convention independence by associating data types and function-return types in the generated stub files and header files with definitions that are specific to each platform.</span></span> <span data-ttu-id="c67a6-106">Эти определения макросов гарантируют, что все типы данных и функции, требующие **\_ \_ разработки, задаются** в качестве объектов.</span><span class="sxs-lookup"><span data-stu-id="c67a6-106">These macro definitions ensure that any data types and functions that require the designation of **\_\_far** are specified as far objects.</span></span>

<span data-ttu-id="c67a6-107">На следующем рисунке показаны определения макросов, применяемые компилятором MIDL для вызовов функций между компонентами RPC:</span><span class="sxs-lookup"><span data-stu-id="c67a6-107">The following figure shows the macro definitions that the MIDL compiler applies to function calls between RPC components:</span></span>

![Схема, на которой показаны определения макросов MIDL, применимые к вызовам функций.](images/prog-a29.png)

<span data-ttu-id="c67a6-109">Макросы RPC определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="c67a6-109">RPC macros are defined as follows.</span></span>



| <span data-ttu-id="c67a6-110">Определение</span><span class="sxs-lookup"><span data-stu-id="c67a6-110">Definition</span></span>    | <span data-ttu-id="c67a6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="c67a6-111">Description</span></span>                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c67a6-112">\_\_\_API RPC</span><span class="sxs-lookup"><span data-stu-id="c67a6-112">\_\_RPC\_API</span></span>  | <span data-ttu-id="c67a6-113">Применяется к вызовам, сделанным заглушкой для пользовательского приложения.</span><span class="sxs-lookup"><span data-stu-id="c67a6-113">Applied to calls made by the stub to the user application.</span></span> <span data-ttu-id="c67a6-114">Обе функции находятся в одной и той же исполняемой программе.</span><span class="sxs-lookup"><span data-stu-id="c67a6-114">Both functions are in the same executable program.</span></span>                                       |
| <span data-ttu-id="c67a6-115">\_\_удаленный \_ RPC</span><span class="sxs-lookup"><span data-stu-id="c67a6-115">\_\_RPC\_FAR</span></span>  | <span data-ttu-id="c67a6-116">Применяется к стандартному определению макроса для указателей.</span><span class="sxs-lookup"><span data-stu-id="c67a6-116">Applied to the standard macro definition for pointers.</span></span> <span data-ttu-id="c67a6-117">Это определение макроса должно отображаться как часть сигнатуры всех предоставляемых пользователем функций.</span><span class="sxs-lookup"><span data-stu-id="c67a6-117">This macro definition should appear as part of the signature of all user-supplied functions.</span></span> |
| <span data-ttu-id="c67a6-118">\_\_\_заглушка RPC</span><span class="sxs-lookup"><span data-stu-id="c67a6-118">\_\_RPC\_STUB</span></span> | <span data-ttu-id="c67a6-119">Применяется к вызовам, сделанным из библиотеки времени выполнения в заглушку.</span><span class="sxs-lookup"><span data-stu-id="c67a6-119">Applied to calls made from the run-time library to the stub.</span></span> <span data-ttu-id="c67a6-120">Эти вызовы можно считать частными.</span><span class="sxs-lookup"><span data-stu-id="c67a6-120">These calls can be considered private.</span></span>                                                 |
| <span data-ttu-id="c67a6-121">\_\_\_пользователь RPC</span><span class="sxs-lookup"><span data-stu-id="c67a6-121">\_\_RPC\_USER</span></span> | <span data-ttu-id="c67a6-122">Применяется к вызовам, выполненным библиотекой времени выполнения для пользовательского приложения.</span><span class="sxs-lookup"><span data-stu-id="c67a6-122">Applied to calls made by the run-time library to the user application.</span></span> <span data-ttu-id="c67a6-123">Они пересекают границу между библиотекой DLL и приложением.</span><span class="sxs-lookup"><span data-stu-id="c67a6-123">These cross the boundary between a DLL and an application.</span></span>                   |
| <span data-ttu-id="c67a6-124">\_запись RPC</span><span class="sxs-lookup"><span data-stu-id="c67a6-124">RPC\_ENTRY</span></span>    | <span data-ttu-id="c67a6-125">Применяется к вызовам, выполненным приложением или заглушкой к библиотеке времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="c67a6-125">Applied to calls made by the application or stub to the run-time library.</span></span> <span data-ttu-id="c67a6-126">Это определение макроса применяется ко всем функциям времени выполнения RPC.</span><span class="sxs-lookup"><span data-stu-id="c67a6-126">This macro definition is applied to all RPC run-time functions.</span></span>           |



 

<span data-ttu-id="c67a6-127">Для правильной связи с библиотеками времени выполнения Microsoft RPC, заглушками и подпрограммами поддержки, некоторые функции, предоставляемые пользователем, также должны включать эти макросы в определение функции.</span><span class="sxs-lookup"><span data-stu-id="c67a6-127">To link correctly with the Microsoft RPC run-time libraries, stubs, and support routines, some user-supplied functions must also include these macros in the function definition.</span></span> <span data-ttu-id="c67a6-128">Используйте **\_ \_ \_ API** макроса RPC при определении функций, связанных с управлением памятью, пользовательскими дескрипторами привязки и атрибутом **передачи \_ as** , а также с помощью макроса **\_ \_ RPC- \_ пользователя** при определении подпрограммы запуска контекста, связанной с дескриптором контекста.</span><span class="sxs-lookup"><span data-stu-id="c67a6-128">Use the macro **\_\_RPC\_API** when you define the functions associated with memory management, user-defined binding handles, and the **transmit\_as** attribute, and use the macro **\_\_RPC\_USER** when you define the context run-down routine associated with the context handle.</span></span> <span data-ttu-id="c67a6-129">Укажите следующие функции:</span><span class="sxs-lookup"><span data-stu-id="c67a6-129">Specify the functions as:</span></span>

<dl> <dt>

<span data-ttu-id="c67a6-130"><span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_Пользователь \_ *MIDL \_* \_ (...) пользователя RPC User (...)</span><span class="sxs-lookup"><span data-stu-id="c67a6-130"><span id="__RPC_USER_midl_user_allocate_..._"></span><span id="__rpc_user_midl_user_allocate_..._"></span><span id="__RPC_USER_MIDL_USER_ALLOCATE_..._"></span>\_\_RPC\_USER *midl\_user*\_allocate(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c67a6-131"><span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_\_Бесплатный пользователь *MIDL \_* RPC \_ (...)</span><span class="sxs-lookup"><span data-stu-id="c67a6-131"><span id="__RPC_USER_midl_user_free_..._"></span><span id="__rpc_user_midl_user_free_..._"></span><span id="__RPC_USER_MIDL_USER_FREE_..._"></span>\_\_RPC\_USER *midl\_user*\_free(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c67a6-132"><span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_RPC \_ user *параметром handletype* \_ BIND (...)</span><span class="sxs-lookup"><span data-stu-id="c67a6-132"><span id="__RPC_USER__handletype_bind_..._"></span><span id="__rpc_user__handletype_bind_..._"></span><span id="__RPC_USER__HANDLETYPE_BIND_..._"></span>\_\_RPC\_USER  *handletype*\_bind(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c67a6-133"><span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_RPC \_ -пользователь *параметром handletype* \_ отменить привязку (...)</span><span class="sxs-lookup"><span data-stu-id="c67a6-133"><span id="__RPC_USER_handletype_unbind_..._"></span><span id="__rpc_user_handletype_unbind_..._"></span><span id="__RPC_USER_HANDLETYPE_UNBIND_..._"></span>\_\_RPC\_USER *handletype*\_unbind(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c67a6-134"><span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_\_ *Тип* пользователя RPC — \_ \_ локальный</span><span class="sxs-lookup"><span data-stu-id="c67a6-134"><span id="__RPC_USER_type_to_local"></span><span id="__rpc_user_type_to_local"></span><span id="__RPC_USER_TYPE_TO_LOCAL"></span>\_\_RPC\_USER *type*\_to\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c67a6-135"><span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_\_ *Тип* пользователя RPC \_ из \_ локальной службы</span><span class="sxs-lookup"><span data-stu-id="c67a6-135"><span id="__RPC_USER_type_from_local"></span><span id="__rpc_user_type_from_local"></span><span id="__RPC_USER_TYPE_FROM_LOCAL"></span>\_\_RPC\_USER *type*\_from\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c67a6-136"><span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_\_Тип пользователя RPC \_ для \_ xmit (...)</span><span class="sxs-lookup"><span data-stu-id="c67a6-136"><span id="__RPC_USER_type_to_xmit_..._"></span><span id="__rpc_user_type_to_xmit_..._"></span><span id="__RPC_USER_TYPE_TO_XMIT_..._"></span>\_\_RPC\_USER type\_to\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c67a6-137"><span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_\_ *Тип* пользователя RPC \_ из \_ xmit (...)</span><span class="sxs-lookup"><span data-stu-id="c67a6-137"><span id="__RPC_USER_type_from_xmit_..._"></span><span id="__rpc_user_type_from_xmit_..._"></span><span id="__RPC_USER_TYPE_FROM_XMIT_..._"></span>\_\_RPC\_USER *type*\_from\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c67a6-138"><span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_\_Бесплатный локальный *тип* пользователя RPC \_ \_</span><span class="sxs-lookup"><span data-stu-id="c67a6-138"><span id="__RPC_USER_type_free_local"></span><span id="__rpc_user_type_free_local"></span><span id="__RPC_USER_TYPE_FREE_LOCAL"></span>\_\_RPC\_USER *type*\_free\_local</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c67a6-139"><span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_\_ *Тип* пользователя RPC \_ Free \_ Inst (...)</span><span class="sxs-lookup"><span data-stu-id="c67a6-139"><span id="__RPC_USER_type_free_inst_..._"></span><span id="__rpc_user_type_free_inst_..._"></span><span id="__RPC_USER_TYPE_FREE_INST_..._"></span>\_\_RPC\_USER *type*\_free\_inst(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c67a6-140"><span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_\_ *Тип* пользователя RPC \_ Free \_ xmit (...)</span><span class="sxs-lookup"><span data-stu-id="c67a6-140"><span id="__RPC_USER_type_free_xmit_..._"></span><span id="__rpc_user_type_free_xmit_..._"></span><span id="__RPC_USER_TYPE_FREE_XMIT_..._"></span>\_\_RPC\_USER *type*\_free\_xmit(...)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c67a6-141"><span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_\_Очистка контекста пользователя RPC \_ (...)</span><span class="sxs-lookup"><span data-stu-id="c67a6-141"><span id="__RPC_USER_context_rundown_..._"></span><span id="__rpc_user_context_rundown_..._"></span><span id="__RPC_USER_CONTEXT_RUNDOWN_..._"></span>\_\_RPC\_USER context\_rundown(...)</span></span>
<span data-ttu-id="c67a6-142"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c67a6-142"></dt> <dd></dd> </dl></span></span>

> [!Note]  
> <span data-ttu-id="c67a6-143">Все параметры указателя в этих функциях должны быть указаны с помощью макроса **\_ \_ RPC \_**.</span><span class="sxs-lookup"><span data-stu-id="c67a6-143">All pointer parameters in these functions must be specified using the macro **\_\_RPC\_FAR**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c67a6-144">Требования</span><span class="sxs-lookup"><span data-stu-id="c67a6-144">Requirements</span></span>



| <span data-ttu-id="c67a6-145">Требование</span><span class="sxs-lookup"><span data-stu-id="c67a6-145">Requirement</span></span> | <span data-ttu-id="c67a6-146">Значение</span><span class="sxs-lookup"><span data-stu-id="c67a6-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c67a6-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c67a6-147">Minimum supported client</span></span><br/> | <span data-ttu-id="c67a6-148">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c67a6-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c67a6-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c67a6-149">Minimum supported server</span></span><br/> | <span data-ttu-id="c67a6-150">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c67a6-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c67a6-151">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c67a6-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="c67a6-152"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="c67a6-152"><dt>Rpc.h</dt></span></span> </dl> |



 

 





