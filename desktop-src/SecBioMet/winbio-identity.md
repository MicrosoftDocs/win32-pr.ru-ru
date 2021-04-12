---
title: Структура WINBIO_IDENTITY (Винбио \_ types. h)
description: Содержит идентифицирующее значение, связанное с биометрической шаблоном.
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- API структуры WINBIO_IDENTITY биометрическая платформа Windows
topic_type:
- apiref
api_name:
- WINBIO_IDENTITY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8092754b9107029e0be5800bbd5bc98bc3efb91c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136110"
---
# <a name="winbio_identity-structure"></a><span data-ttu-id="1634e-104">\_Структура идентификации винбио</span><span class="sxs-lookup"><span data-stu-id="1634e-104">WINBIO\_IDENTITY structure</span></span>

<span data-ttu-id="1634e-105">Структура **\_ удостоверения винбио** содержит идентифицирующее значение, связанное с биометрической шаблоном.</span><span class="sxs-lookup"><span data-stu-id="1634e-105">The **WINBIO\_IDENTITY** structure contains an identifying value associated with a biometric template.</span></span>

## <a name="syntax"></a><span data-ttu-id="1634e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1634e-106">Syntax</span></span>


```C++
typedef struct _WINBIO_IDENTITY {
  WINBIO_IDENTITY_TYPE Type;
  union {
    ULONG  Null;
    ULONG  Wildcard;
    GUID   TemplateGuid;
    struct {
      ULONG Size;
      UCHAR Data[SECURITY_MAX_SID_SIZE];
    } AccountSid;
  } Value;
} WINBIO_IDENTITY;
```



## <a name="members"></a><span data-ttu-id="1634e-107">Члены</span><span class="sxs-lookup"><span data-stu-id="1634e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1634e-108">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1634e-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="1634e-109">Задает формат сведений об удостоверении, содержащихся в этой структуре.</span><span class="sxs-lookup"><span data-stu-id="1634e-109">Specifies the format of the identity information contained in this structure.</span></span> <span data-ttu-id="1634e-110">Может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="1634e-110">This can be one of the following values:</span></span>



| <span data-ttu-id="1634e-111">Значение</span><span class="sxs-lookup"><span data-stu-id="1634e-111">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="1634e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="1634e-112">Meaning</span></span>                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <span data-ttu-id="1634e-113"><dt>**\_тип идентификатора \_ винбио \_ null**</dt></span><span class="sxs-lookup"><span data-stu-id="1634e-113"><dt>**WINBIO\_ID\_TYPE\_NULL**</dt></span></span> </dl>             | <span data-ttu-id="1634e-114">Шаблон не имеет связанного идентификатора.</span><span class="sxs-lookup"><span data-stu-id="1634e-114">The template has no associated ID.</span></span><br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <span data-ttu-id="1634e-115"><dt>**\_ \_ шаблон типа идентификатора \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="1634e-115"><dt>**WINBIO\_ID\_TYPE\_WILDCARD**</dt></span></span> </dl> | <span data-ttu-id="1634e-116">Структура соответствует всем удостоверениям шаблона.</span><span class="sxs-lookup"><span data-stu-id="1634e-116">The structure matches all template identities.</span></span><br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <span data-ttu-id="1634e-117"><dt>**\_ \_ GUID типа идентификатора \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="1634e-117"><dt>**WINBIO\_ID\_TYPE\_GUID**</dt></span></span> </dl>             | <span data-ttu-id="1634e-118">Структура содержит идентификатор GUID, связанный с шаблоном.</span><span class="sxs-lookup"><span data-stu-id="1634e-118">The structure contains a GUID associated with the template.</span></span><br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <span data-ttu-id="1634e-119"><dt>**ИД \_ \_ безопасности типа \_ идентификатора винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="1634e-119"><dt>**WINBIO\_ID\_TYPE\_SID**</dt></span></span> </dl>                | <span data-ttu-id="1634e-120">Структура содержит идентификатор безопасности учетной записи, связанный с шаблоном.</span><span class="sxs-lookup"><span data-stu-id="1634e-120">The structure contains the account SID associated with the template.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1634e-121">**Значение**</span><span class="sxs-lookup"><span data-stu-id="1634e-121">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="1634e-122">Объединение, которое может содержать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="1634e-122">A union that can contain one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="1634e-123">**Null**</span><span class="sxs-lookup"><span data-stu-id="1634e-123">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="1634e-124">Содержит 1, если член **типа** имеет **\_ тип винбио \_ ID \_ null**.</span><span class="sxs-lookup"><span data-stu-id="1634e-124">Contains 1 if the **Type** member is **WINBIO\_ID\_TYPE\_NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1634e-125">**Подстановочный знак**</span><span class="sxs-lookup"><span data-stu-id="1634e-125">**Wildcard**</span></span>
</dt> <dd>

<span data-ttu-id="1634e-126">Содержит значение 1, если член **типа** имеет **\_ \_ \_ подстановочный знак винбио типа ID**.</span><span class="sxs-lookup"><span data-stu-id="1634e-126">Contains 1 if the **Type** member is **WINBIO\_ID\_TYPE\_WILDCARD**.</span></span>

</dd> <dt>

<span data-ttu-id="1634e-127">**темплатегуид**</span><span class="sxs-lookup"><span data-stu-id="1634e-127">**TemplateGuid**</span></span>
</dt> <dd>

<span data-ttu-id="1634e-128">Содержит 128-разрядное значение идентификатора GUID, идентифицирующее шаблон, если член **типа** имеет тип **винбио \_ ID \_ \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="1634e-128">Contains a 128-bit GUID value that identifies the template if the **Type** member is **WINBIO\_ID\_TYPE\_GUID**.</span></span>

</dd> <dt>

<span data-ttu-id="1634e-129">**AccountSid**</span><span class="sxs-lookup"><span data-stu-id="1634e-129">**AccountSid**</span></span>
</dt> <dd>

<span data-ttu-id="1634e-130">Структура, содержащая идентификатор безопасности учетной записи, если член **типа** имеет **\_ тип винбио ID \_ \_ SID**.</span><span class="sxs-lookup"><span data-stu-id="1634e-130">A structure that contains an account SID if the **Type** member is **WINBIO\_ID\_TYPE\_SID**.</span></span>

<dl> <dt>

<span data-ttu-id="1634e-131">**Размер**</span><span class="sxs-lookup"><span data-stu-id="1634e-131">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="1634e-132">Число символов в SID.</span><span class="sxs-lookup"><span data-stu-id="1634e-132">The number of characters in the SID.</span></span>

</dd> <dt>

<span data-ttu-id="1634e-133">**Data**</span><span class="sxs-lookup"><span data-stu-id="1634e-133">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="1634e-134">Массив неподписанных символов, содержащих идентификатор безопасности.</span><span class="sxs-lookup"><span data-stu-id="1634e-134">An array of unsigned characters that contain the SID.</span></span> <span data-ttu-id="1634e-135">Текущий максимальный размер массива составляет 68 символов.</span><span class="sxs-lookup"><span data-stu-id="1634e-135">The current maximum size of the array is 68 characters.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1634e-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1634e-136">Remarks</span></span>

<span data-ttu-id="1634e-137">Эта структура используется в следующих функциях:</span><span class="sxs-lookup"><span data-stu-id="1634e-137">This structure is used in the following functions:</span></span>

-   [<span data-ttu-id="1634e-138">**винбиоделететемплате**</span><span class="sxs-lookup"><span data-stu-id="1634e-138">**WinBioDeleteTemplate**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)
-   [<span data-ttu-id="1634e-139">**винбиоенроллкоммит**</span><span class="sxs-lookup"><span data-stu-id="1634e-139">**WinBioEnrollCommit**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)
-   [<span data-ttu-id="1634e-140">**винбиоенуменроллментс**</span><span class="sxs-lookup"><span data-stu-id="1634e-140">**WinBioEnumEnrollments**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)
-   [<span data-ttu-id="1634e-141">**винбиожеткредентиалстате**</span><span class="sxs-lookup"><span data-stu-id="1634e-141">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
-   [<span data-ttu-id="1634e-142">**винбиоидентифи**</span><span class="sxs-lookup"><span data-stu-id="1634e-142">**WinBioIdentify**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)
-   [<span data-ttu-id="1634e-143">**винбиоремовекредентиал**</span><span class="sxs-lookup"><span data-stu-id="1634e-143">**WinBioRemoveCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
-   [<span data-ttu-id="1634e-144">**винбиоверифи**</span><span class="sxs-lookup"><span data-stu-id="1634e-144">**WinBioVerify**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioverify)
-   [<span data-ttu-id="1634e-145">**винбиоверифивискаллбакк**</span><span class="sxs-lookup"><span data-stu-id="1634e-145">**WinBioVerifyWithCallback**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)

## <a name="requirements"></a><span data-ttu-id="1634e-146">Требования</span><span class="sxs-lookup"><span data-stu-id="1634e-146">Requirements</span></span>



| <span data-ttu-id="1634e-147">Требование</span><span class="sxs-lookup"><span data-stu-id="1634e-147">Requirement</span></span> | <span data-ttu-id="1634e-148">Значение</span><span class="sxs-lookup"><span data-stu-id="1634e-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1634e-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1634e-149">Minimum supported client</span></span><br/> | <span data-ttu-id="1634e-150">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1634e-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="1634e-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1634e-151">Minimum supported server</span></span><br/> | <span data-ttu-id="1634e-152">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1634e-152">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1634e-153">Header</span><span class="sxs-lookup"><span data-stu-id="1634e-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="1634e-154"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1634e-154"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1634e-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1634e-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1634e-156">Структуры клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="1634e-156">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





