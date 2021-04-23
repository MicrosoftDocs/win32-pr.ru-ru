---
description: Создает SSL набор ключей сеанса протокола SSL.
ms.assetid: 88465f30-8591-411e-8618-8a381d4c22e9
title: Функция Сслженератесессионкэйс (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateSessionKeys
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cf8e20008d2a77cae3a47728f4e38fff8ae0b09b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664728"
---
# <a name="sslgeneratesessionkeys-function"></a><span data-ttu-id="f04b7-103">Функция Сслженератесессионкэйс</span><span class="sxs-lookup"><span data-stu-id="f04b7-103">SslGenerateSessionKeys function</span></span>

<span data-ttu-id="f04b7-104">Функция **сслженератесессионкэйс** создает SSL набор ключей сеанса [*протокола*](/windows/desktop/SecGloss/s-gly) SSL.</span><span class="sxs-lookup"><span data-stu-id="f04b7-104">The **SslGenerateSessionKeys** function generates a set of [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) session keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="f04b7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f04b7-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGenerateSessionKeys(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _Out_ NCRYPT_KEY_HANDLE  *phReadKey,
  _Out_ NCRYPT_KEY_HANDLE  *phWriteKey,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f04b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f04b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f04b7-107">*хсслпровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f04b7-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04b7-108">Обработчик для экземпляра поставщика протокола SSL.</span><span class="sxs-lookup"><span data-stu-id="f04b7-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="f04b7-109">*хмастеркэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f04b7-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04b7-110">Маркер для объекта [*главного ключа*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="f04b7-110">The handle to the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="f04b7-111">*фреадкэй* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f04b7-111">*phReadKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f04b7-112">Указатель на возвращаемый маркер считывания ключа.</span><span class="sxs-lookup"><span data-stu-id="f04b7-112">A pointer to the returned read key handle.</span></span>

</dd> <dt>

<span data-ttu-id="f04b7-113">*фвритекэй* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f04b7-113">*phWriteKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f04b7-114">Указатель на возвращенный обработчик ключа записи.</span><span class="sxs-lookup"><span data-stu-id="f04b7-114">A pointer to the returned write key handle.</span></span>

</dd> <dt>

<span data-ttu-id="f04b7-115">*ппараметерлист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f04b7-115">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04b7-116">Указатель на массив буферов [**нкриптбуффер**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) , содержащих сведения, используемые в рамках операции обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="f04b7-116">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="f04b7-117">Точный набор буферов зависит от используемого протокола и набора шифров.</span><span class="sxs-lookup"><span data-stu-id="f04b7-117">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="f04b7-118">По крайней мере, список будет содержать буферы, содержащие клиентские и серверные случайные значения.</span><span class="sxs-lookup"><span data-stu-id="f04b7-118">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="f04b7-119">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f04b7-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04b7-120">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="f04b7-120">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f04b7-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f04b7-121">Return value</span></span>

<span data-ttu-id="f04b7-122">Если функция завершается с ошибкой, она возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="f04b7-122">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="f04b7-123">Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="f04b7-123">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="f04b7-124">Возможные коды возврата включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="f04b7-124">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="f04b7-125">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="f04b7-125">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="f04b7-126">Описание</span><span class="sxs-lookup"><span data-stu-id="f04b7-126">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f04b7-127">Не <dt>**превышать \_ НЕТ \_**</dt> <dt>0x8009000EL</dt> памяти</span><span class="sxs-lookup"><span data-stu-id="f04b7-127"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="f04b7-128">Недостаточно памяти для выделения необходимых буферов.</span><span class="sxs-lookup"><span data-stu-id="f04b7-128">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="f04b7-129">Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f04b7-129"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="f04b7-130">Один из указанных дескрипторов недопустим.</span><span class="sxs-lookup"><span data-stu-id="f04b7-130">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="f04b7-131">Не <dt>**превышать \_ Недопустимый \_ параметр**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="f04b7-131"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="f04b7-132">Параметр *фреадкэй* или *фвритекэй* имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="f04b7-132">The *phReadKey* or *phWriteKey* parameter is null.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="f04b7-133">Требования</span><span class="sxs-lookup"><span data-stu-id="f04b7-133">Requirements</span></span>



| <span data-ttu-id="f04b7-134">Требование</span><span class="sxs-lookup"><span data-stu-id="f04b7-134">Requirement</span></span> | <span data-ttu-id="f04b7-135">Значение</span><span class="sxs-lookup"><span data-stu-id="f04b7-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f04b7-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f04b7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f04b7-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f04b7-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f04b7-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f04b7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f04b7-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f04b7-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f04b7-140">Header</span><span class="sxs-lookup"><span data-stu-id="f04b7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f04b7-141"><dt>Сслпровидер. h</dt></span><span class="sxs-lookup"><span data-stu-id="f04b7-141"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="f04b7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f04b7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f04b7-143"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f04b7-143"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

