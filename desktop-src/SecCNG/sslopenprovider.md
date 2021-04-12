---
description: Открывает маркер для SSL указанного поставщика протокола SSL.
ms.assetid: 0d5c4da3-12d6-4a53-a4d0-f0f174a4c8d8
title: Функция Сслопенпровидер (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenProvider
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8a9ea6c97662d94fffef0c87a227d5e2ae052606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262996"
---
# <a name="sslopenprovider-function"></a><span data-ttu-id="84f95-103">Функция Сслопенпровидер</span><span class="sxs-lookup"><span data-stu-id="84f95-103">SslOpenProvider function</span></span>

<span data-ttu-id="84f95-104">Функция **сслопенпровидер** открывает маркер для [*SSL*](/windows/desktop/SecGloss/s-gly) указанного поставщика протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="84f95-104">The **SslOpenProvider** function opens a handle to the specified [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f95-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84f95-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslOpenProvider(
  _Out_ NCRYPT_PROV_HANDLE *phSslProvider,
  _In_  LPCWSTR            pszProviderName,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="84f95-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="84f95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84f95-107">*фсслпровидер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="84f95-107">*phSslProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84f95-108">Адрес **\_ \_ маркера NCRYPT Prov** , в который записывается маркер поставщика.</span><span class="sxs-lookup"><span data-stu-id="84f95-108">The address of an **NCRYPT\_PROV\_HANDLE** in which to write the provider handle.</span></span>

<span data-ttu-id="84f95-109">По завершении использования маркера его необходимо освободить, вызвав функцию [**сслфриобжект**](sslfreeobject.md) .</span><span class="sxs-lookup"><span data-stu-id="84f95-109">When you have finished using the handle, you should free it by calling the [**SslFreeObject**](sslfreeobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="84f95-110">*псзпровидернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84f95-110">*pszProviderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84f95-111">Указатель на строку в Юникоде, содержащую имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="84f95-111">A pointer to a Unicode string that contains the provider name.</span></span> <span data-ttu-id="84f95-112">Если значение этого параметра равно **null**, возвращается маркер **\_ \_ поставщика MS SChannel** .</span><span class="sxs-lookup"><span data-stu-id="84f95-112">If the value of this parameter is **NULL**, a handle to the **MS\_SCHANNEL\_PROVIDER** is returned.</span></span>

</dd> <dt>

<span data-ttu-id="84f95-113">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84f95-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84f95-114">Этот параметр зарезервирован для будущего использования и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="84f95-114">This parameter is reserved for future use, and it must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84f95-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84f95-115">Return value</span></span>

<span data-ttu-id="84f95-116">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="84f95-116">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="84f95-117">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="84f95-117">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="84f95-118">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="84f95-118">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="84f95-119">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="84f95-119">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="84f95-120">Описание</span><span class="sxs-lookup"><span data-stu-id="84f95-120">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="84f95-121">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="84f95-121"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="84f95-122">Один из указанных дескрипторов недопустим.</span><span class="sxs-lookup"><span data-stu-id="84f95-122">One of the provided handles is not valid.</span></span><br/>                      |
| <dl> <span data-ttu-id="84f95-123">Не <dt>**превышать \_ Недопустимый \_ параметр**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="84f95-123"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="84f95-124">Параметр *фсслпровидер* или *Пппровидерлист* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="84f95-124">The *phSslProvider* or *ppProviderList* parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="84f95-125"><dt>**Состояние \_ НЕТ \_**</dt> <dt>0xC0000017L</dt> памяти</span><span class="sxs-lookup"><span data-stu-id="84f95-125"><dt>**STATUS\_NO\_MEMORY**</dt> <dt>0xC0000017L</dt></span></span> </dl>      | <span data-ttu-id="84f95-126">Недостаточно памяти для выделения необходимых буферов.</span><span class="sxs-lookup"><span data-stu-id="84f95-126">Not enough memory is available to allocate necessary buffers.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="84f95-127">Требования</span><span class="sxs-lookup"><span data-stu-id="84f95-127">Requirements</span></span>



| <span data-ttu-id="84f95-128">Требование</span><span class="sxs-lookup"><span data-stu-id="84f95-128">Requirement</span></span> | <span data-ttu-id="84f95-129">Значение</span><span class="sxs-lookup"><span data-stu-id="84f95-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="84f95-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84f95-130">Minimum supported client</span></span><br/> | <span data-ttu-id="84f95-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84f95-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="84f95-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84f95-132">Minimum supported server</span></span><br/> | <span data-ttu-id="84f95-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="84f95-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="84f95-134">Header</span><span class="sxs-lookup"><span data-stu-id="84f95-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="84f95-135"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="84f95-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="84f95-136">DLL</span><span class="sxs-lookup"><span data-stu-id="84f95-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84f95-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84f95-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

