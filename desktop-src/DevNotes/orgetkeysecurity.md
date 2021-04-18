---
description: Извлекает копию дескриптора безопасности, защищающего указанный открытый раздел реестра, в автономном кусте реестра.
ms.assetid: 676d5be5-d9d8-48c6-848a-917d1a0474c6
title: Функция Оржеткэйсекурити (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 13594493af2e7992471d13dce30f0a848501c4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648895"
---
# <a name="orgetkeysecurity-function"></a><span data-ttu-id="4aa6a-103">Функция Оржеткэйсекурити</span><span class="sxs-lookup"><span data-stu-id="4aa6a-103">ORGetKeySecurity function</span></span>

<span data-ttu-id="4aa6a-104">Извлекает копию дескриптора безопасности, защищающего указанный открытый раздел реестра, в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="4aa6a-104">Retrieves a copy of the security descriptor protecting the specified open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aa6a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4aa6a-105">Syntax</span></span>


```C++
DWORD ORGetKeySecurity(
  _In_      ORHKEY               Handle,
  _In_      SECURITY_INFORMATION SecurityInformation,
  _Out_opt_ PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Inout_   PDWORD               lpcbSecurityDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="4aa6a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4aa6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aa6a-107">*Обработчик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4aa6a-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4aa6a-108">Маркер открытого раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="4aa6a-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="4aa6a-109">*Секуритинформатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4aa6a-109">*SecurityInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4aa6a-110">Значение [ \_ сведений о безопасности](../secauthz/security-information.md) , указывающее запрошенные сведения о безопасности.</span><span class="sxs-lookup"><span data-stu-id="4aa6a-110">A [SECURITY\_INFORMATION](../secauthz/security-information.md) value that indicates the requested security information.</span></span>

</dd> <dt>

<span data-ttu-id="4aa6a-111">*псекуритидескриптор* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="4aa6a-111">*pSecurityDescriptor* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4aa6a-112">Указатель на буфер, который получает копию запрошенного дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="4aa6a-112">A pointer to a buffer that receives a copy of the requested security descriptor.</span></span> <span data-ttu-id="4aa6a-113">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4aa6a-113">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4aa6a-114">*лпкбсекуритидескриптор* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="4aa6a-114">*lpcbSecurityDescriptor* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4aa6a-115">Указатель на переменную, указывающую размер (в байтах) буфера, на который указывает параметр *псекуритидескриптор* .</span><span class="sxs-lookup"><span data-stu-id="4aa6a-115">A pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the *pSecurityDescriptor* parameter.</span></span> <span data-ttu-id="4aa6a-116">Когда функция возвращает значение, переменная содержит число байтов, записанных в буфер.</span><span class="sxs-lookup"><span data-stu-id="4aa6a-116">When the function returns, the variable contains the number of bytes written to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aa6a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4aa6a-117">Return value</span></span>

<span data-ttu-id="4aa6a-118">Если функция завершается успешно, функция возвращает ошибку \_ Success.</span><span class="sxs-lookup"><span data-stu-id="4aa6a-118">If the function succeeds, the function returns ERROR\_SUCCESS.</span></span>

<span data-ttu-id="4aa6a-119">Если функция завершается ошибкой, она возвращает ненулевой код ошибки, определенный в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="4aa6a-119">If the function fails, it returns a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="4aa6a-120">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.</span><span class="sxs-lookup"><span data-stu-id="4aa6a-120">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="4aa6a-121">Если буфер, указанный в параметре *псекуритидескриптор* , слишком мал, функция возвращает ошибку \_ недостаточный \_ Размер буфера, а параметр *лпкбсекуритидескриптор* содержит число байтов, необходимое для запрошенного дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="4aa6a-121">If the buffer specified by the *pSecurityDescriptor* parameter is too small, the function returns ERROR\_INSUFFICIENT\_BUFFER and the *lpcbSecurityDescriptor* parameter contains the number of bytes required for the requested security descriptor.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aa6a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="4aa6a-122">Requirements</span></span>



| <span data-ttu-id="4aa6a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="4aa6a-123">Requirement</span></span> | <span data-ttu-id="4aa6a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4aa6a-124">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4aa6a-125">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="4aa6a-125">Redistributable</span></span><br/> | <span data-ttu-id="4aa6a-126">Автономная библиотека реестра Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="4aa6a-126">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="4aa6a-127">Header</span><span class="sxs-lookup"><span data-stu-id="4aa6a-127">Header</span></span><br/>          | <dl> <span data-ttu-id="4aa6a-128"><dt>Оффрег. h</dt></span><span class="sxs-lookup"><span data-stu-id="4aa6a-128"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="4aa6a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4aa6a-129">DLL</span></span><br/>             | <dl> <span data-ttu-id="4aa6a-130"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4aa6a-130"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aa6a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4aa6a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aa6a-132">**орделетекэй**</span><span class="sxs-lookup"><span data-stu-id="4aa6a-132">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="4aa6a-133">**оропенкэй**</span><span class="sxs-lookup"><span data-stu-id="4aa6a-133">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="4aa6a-134">**орсеткэйсекурити**</span><span class="sxs-lookup"><span data-stu-id="4aa6a-134">**ORSetKeySecurity**</span></span>](orsetkeysecurity.md)
</dt> <dt>

[<span data-ttu-id="4aa6a-135">\_сведения о безопасности</span><span class="sxs-lookup"><span data-stu-id="4aa6a-135">SECURITY\_INFORMATION</span></span>](../secauthz/security-information.md)
</dt> </dl>

 

 
