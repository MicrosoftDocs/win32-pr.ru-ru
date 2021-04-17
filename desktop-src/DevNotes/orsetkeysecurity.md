---
description: Задает безопасность открытого раздела реестра в автономном кусте реестра.
ms.assetid: 002866bb-1532-41ad-a4db-a32d6e1c0a6a
title: Функция Орсеткэйсекурити (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ff63a7d896964f486b5fcb168c08513f8d5703be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665119"
---
# <a name="orsetkeysecurity-function"></a><span data-ttu-id="da4d3-103">Функция Орсеткэйсекурити</span><span class="sxs-lookup"><span data-stu-id="da4d3-103">ORSetKeySecurity function</span></span>

<span data-ttu-id="da4d3-104">Задает безопасность открытого раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="da4d3-104">Sets the security of an open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="da4d3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da4d3-105">Syntax</span></span>


```C++
DWORD ORSetKeySecurity(
  _In_ ORHKEY               Handle,
  _In_ SECURITY_INFORMATION SecurityInformation,
  _In_ PSECURITY_DESCRIPTOR pSecurityDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="da4d3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="da4d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da4d3-107">*Обработчик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da4d3-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da4d3-108">Маркер открытого раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="da4d3-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="da4d3-109">*Секуритинформатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da4d3-109">*SecurityInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da4d3-110">Битовые флаги, указывающие тип сведений о безопасности для установки.</span><span class="sxs-lookup"><span data-stu-id="da4d3-110">Bit flags that indicate the type of security information to set.</span></span> <span data-ttu-id="da4d3-111">Этот параметр может быть сочетанием битовых флагов [ \_ сведений о безопасности](../secauthz/security-information.md) .</span><span class="sxs-lookup"><span data-stu-id="da4d3-111">This parameter can be a combination of the [SECURITY\_INFORMATION](../secauthz/security-information.md) bit flags.</span></span>

</dd> <dt>

<span data-ttu-id="da4d3-112">*псекуритидескриптор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da4d3-112">*pSecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da4d3-113">Указатель на структуру [ \_ дескриптора безопасности](/windows/win32/api/winnt/ns-winnt-security_descriptor) , указывающую атрибуты безопасности, которые необходимо задать для указанного ключа.</span><span class="sxs-lookup"><span data-stu-id="da4d3-113">A pointer to a [SECURITY\_DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor) structure that specifies the security attributes to set for the specified key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da4d3-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da4d3-114">Return value</span></span>

<span data-ttu-id="da4d3-115">Если функция завершается успешно, функция возвращает ошибку \_ Success.</span><span class="sxs-lookup"><span data-stu-id="da4d3-115">If the function succeeds, the function returns ERROR\_SUCCESS.</span></span>

<span data-ttu-id="da4d3-116">Если функция завершается ошибкой, она возвращает ненулевой код ошибки, определенный в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="da4d3-116">If the function fails, it returns a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="da4d3-117">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.</span><span class="sxs-lookup"><span data-stu-id="da4d3-117">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="da4d3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="da4d3-118">Requirements</span></span>



| <span data-ttu-id="da4d3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="da4d3-119">Requirement</span></span> | <span data-ttu-id="da4d3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="da4d3-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da4d3-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="da4d3-121">Redistributable</span></span><br/> | <span data-ttu-id="da4d3-122">Автономная библиотека реестра Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="da4d3-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="da4d3-123">Header</span><span class="sxs-lookup"><span data-stu-id="da4d3-123">Header</span></span><br/>          | <dl> <span data-ttu-id="da4d3-124"><dt>Оффрег. h</dt></span><span class="sxs-lookup"><span data-stu-id="da4d3-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="da4d3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="da4d3-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="da4d3-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da4d3-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da4d3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da4d3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da4d3-128">**орклосекэй**</span><span class="sxs-lookup"><span data-stu-id="da4d3-128">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="da4d3-129">**орделетекэй**</span><span class="sxs-lookup"><span data-stu-id="da4d3-129">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="da4d3-130">**оропенкэй**</span><span class="sxs-lookup"><span data-stu-id="da4d3-130">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="da4d3-131">**оржеткэйсекурити**</span><span class="sxs-lookup"><span data-stu-id="da4d3-131">**ORGetKeySecurity**</span></span>](orgetkeysecurity.md)
</dt> <dt>

[<span data-ttu-id="da4d3-132">\_дескриптор безопасности</span><span class="sxs-lookup"><span data-stu-id="da4d3-132">SECURITY\_DESCRIPTOR</span></span>](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="da4d3-133">\_сведения о безопасности</span><span class="sxs-lookup"><span data-stu-id="da4d3-133">SECURITY\_INFORMATION</span></span>](../secauthz/security-information.md)
</dt> </dl>

 

 
