---
title: Метод Ивмдрмлиценсеманажемент Креателиценсеревокатиончалленже (Вмдрмсдк. h)
description: Метод Креателиценсеревокатиончалленже создает запрос отзыва лицензии.
ms.assetid: 31fcf7a7-1af8-4474-abac-eddb1070975b
keywords:
- Формат Windows Media, Креателиценсеревокатиончалленже метод
- Креателиценсеревокатиончалленже метод Windows Media Format, интерфейс Ивмдрмлиценсеманажемент
- Интерфейс Ивмдрмлиценсеманажемент Windows Media Format, метод Креателиценсеревокатиончалленже
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseRevocationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7fd0acb41b9a2548e5be708611529bea92e131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717915"
---
# <a name="iwmdrmlicensemanagementcreatelicenserevocationchallenge-method"></a><span data-ttu-id="87e95-106">Метод Ивмдрмлиценсеманажемент:: Креателиценсеревокатиончалленже</span><span class="sxs-lookup"><span data-stu-id="87e95-106">IWMDRMLicenseManagement::CreateLicenseRevocationChallenge method</span></span>

<span data-ttu-id="87e95-107">Метод **креателиценсеревокатиончалленже** создает запрос отзыва лицензии.</span><span class="sxs-lookup"><span data-stu-id="87e95-107">The **CreateLicenseRevocationChallenge** method generates a license revocation challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="87e95-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87e95-108">Syntax</span></span>


```C++
HRESULT CreateLicenseRevocationChallenge(
  [in]  BYTE  *pbMachineID,
  [in]  DWORD cbMachineID,
  [in]  BYTE  *pbChallenge,
  [in]  DWORD cbChallenge,
  [out] BYTE  **ppbChallengeOutput,
  [out] DWORD *pcbChallengeOutput
);
```



## <a name="parameters"></a><span data-ttu-id="87e95-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="87e95-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87e95-110">*пбмачинеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87e95-110">*pbMachineID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87e95-111">Идентификатор компьютера, указанный пользователем.</span><span class="sxs-lookup"><span data-stu-id="87e95-111">User-specified machine identifier.</span></span> <span data-ttu-id="87e95-112">Это значение используется для запроса лицензии на сервере и должно соответствовать любому формату, используемому сервером лицензирования.</span><span class="sxs-lookup"><span data-stu-id="87e95-112">This value is used to query for a license on the server and must conform to whatever format the license server uses.</span></span>

</dd> <dt>

<span data-ttu-id="87e95-113">*кбмачинеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87e95-113">*cbMachineID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87e95-114">Размер (в байтах) идентификатора компьютера.</span><span class="sxs-lookup"><span data-stu-id="87e95-114">Size, in bytes, of the machine identifier.</span></span>

</dd> <dt>

<span data-ttu-id="87e95-115">*пбчалленже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87e95-115">*pbChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87e95-116">Определяемые пользователем данные запроса.</span><span class="sxs-lookup"><span data-stu-id="87e95-116">User-specified challenge data.</span></span> <span data-ttu-id="87e95-117">Эти данные, помимо идентификатора компьютера, используются для запроса сервера лицензирования на отзыв лицензий.</span><span class="sxs-lookup"><span data-stu-id="87e95-117">This data, in addition to the machine identifier, is used to query the license server for licenses to be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="87e95-118">*кбчалленже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87e95-118">*cbChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87e95-119">Размер (в байтах) данных запроса.</span><span class="sxs-lookup"><span data-stu-id="87e95-119">Size, in bytes, of the challenge data.</span></span>

</dd> <dt>

<span data-ttu-id="87e95-120">*ппбчалленжеаутпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="87e95-120">*ppbChallengeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87e95-121">Адрес указателя, получающего адрес вывода запроса.</span><span class="sxs-lookup"><span data-stu-id="87e95-121">Address of a pointer that receives the address of the challenge output.</span></span> <span data-ttu-id="87e95-122">Этот буфер представляет собой данные, отправляемые в службу отзыва лицензий.</span><span class="sxs-lookup"><span data-stu-id="87e95-122">This buffer is the data that is sent to the license revocation service.</span></span> <span data-ttu-id="87e95-123">После завершения работы с этими данными необходимо освободить память, вызвав **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="87e95-123">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="87e95-124">*пкбчалленжеаутпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="87e95-124">*pcbChallengeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87e95-125">Адрес переменной, получающей размер выделенных выходных данных запроса в байтах.</span><span class="sxs-lookup"><span data-stu-id="87e95-125">Address of a variable that receives the size of the allocated challenge output data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87e95-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87e95-126">Return value</span></span>

<span data-ttu-id="87e95-127">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="87e95-127">The method returns an **HRESULT**.</span></span> <span data-ttu-id="87e95-128">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="87e95-128">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="87e95-129">Код возврата</span><span class="sxs-lookup"><span data-stu-id="87e95-129">Return code</span></span>                                                                          | <span data-ttu-id="87e95-130">Описание</span><span class="sxs-lookup"><span data-stu-id="87e95-130">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="87e95-131"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="87e95-131"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="87e95-132">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="87e95-132">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="87e95-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87e95-133">Remarks</span></span>

<span data-ttu-id="87e95-134">Нет.</span><span class="sxs-lookup"><span data-stu-id="87e95-134">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="87e95-135">Требования</span><span class="sxs-lookup"><span data-stu-id="87e95-135">Requirements</span></span>



| <span data-ttu-id="87e95-136">Требование</span><span class="sxs-lookup"><span data-stu-id="87e95-136">Requirement</span></span> | <span data-ttu-id="87e95-137">Значение</span><span class="sxs-lookup"><span data-stu-id="87e95-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87e95-138">Header</span><span class="sxs-lookup"><span data-stu-id="87e95-138">Header</span></span><br/> | <dl> <span data-ttu-id="87e95-139"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="87e95-139"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87e95-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87e95-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87e95-141">**Интерфейс Ивмдрмлиценсеманажемент**</span><span class="sxs-lookup"><span data-stu-id="87e95-141">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





