---
description: Функция Ркэйопенкэйсервице не поддерживается.
ms.assetid: 3af18cf7-bc98-4ebc-a62c-7234e9fbddaa
title: Функция Ркэйопенкэйсервице (Ркэйсвкк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyOpenKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: ce905594d1ed088eb72dc59a1fa6beec576384ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683815"
---
# <a name="rkeyopenkeyservice-function"></a><span data-ttu-id="ecc50-103">Функция Ркэйопенкэйсервице</span><span class="sxs-lookup"><span data-stu-id="ecc50-103">RKeyOpenKeyService function</span></span>

<span data-ttu-id="ecc50-104">Функция **ркэйопенкэйсервице** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ecc50-104">The **RKeyOpenKeyService** function is not supported.</span></span>

<span data-ttu-id="ecc50-105">**Windows Server 2003:** Функция **ркэйопенкэйсервице** устанавливает соединение с удаленным компьютером и открывает маркер службы ключей.</span><span class="sxs-lookup"><span data-stu-id="ecc50-105">**Windows Server 2003:** The **RKeyOpenKeyService** function establishes a connection to a remote computer and opens a key service handle.</span></span> <span data-ttu-id="ecc50-106">Маркер службы ключей может впоследствии использоваться функцией [**ркэйпфксинсталл**](rkeypfxinstall.md) .</span><span class="sxs-lookup"><span data-stu-id="ecc50-106">The key service handle can subsequently be used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span> <span data-ttu-id="ecc50-107">Обратите внимание, что это поведение изменилось в Windows Server 2003 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ecc50-107">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="ecc50-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ecc50-108">Syntax</span></span>


```C++
ULONG RKeyOpenKeyService(
  _In_    LPSTR          pszMachineName,
  _In_    KEYSVC_TYPE    OwnerType,
  _In_    LPWSTR         pwszOwnerName,
  _In_    void           *pAuthentication,
  _Inout_ void           *pReserved,
  _Out_   KEYSVCC_HANDLE *phKeySvcCli
);
```



## <a name="parameters"></a><span data-ttu-id="ecc50-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ecc50-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecc50-110">*псзмачиненаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ecc50-110">*pszMachineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecc50-111">Длинный указатель на строку, завершающуюся нулем, которая представляет компьютер, на котором будет открыт маркер службы ключей.</span><span class="sxs-lookup"><span data-stu-id="ecc50-111">Long pointer to a null-terminated string that represents the computer where the key service handle will be opened.</span></span>

</dd> <dt>

<span data-ttu-id="ecc50-112">*OwnerType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ecc50-112">*OwnerType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecc50-113">[**Кэйсвк \_ Значение типа**](keysvc-type.md) , представляющее тип ключа.</span><span class="sxs-lookup"><span data-stu-id="ecc50-113">[**KEYSVC\_TYPE**](keysvc-type.md) value that represents the key type.</span></span> <span data-ttu-id="ecc50-114">Единственное поддерживаемое значение — **кэйсвкмачине**.</span><span class="sxs-lookup"><span data-stu-id="ecc50-114">The only supported value is **KeySvcMachine**.</span></span>

</dd> <dt>

<span data-ttu-id="ecc50-115">*пвсзовнернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ecc50-115">*pwszOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecc50-116">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="ecc50-116">Reserved.</span></span> <span data-ttu-id="ecc50-117">Присвойте этому параметру значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ecc50-117">Set this value to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ecc50-118">*паусентикатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ecc50-118">*pAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecc50-119">Указатель на **значение типа void** , представляющее параметры проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ecc50-119">A pointer to a **void** that represents the authentication settings.</span></span> <span data-ttu-id="ecc50-120">Этот указатель может указывать на нулевое или следующее значение.</span><span class="sxs-lookup"><span data-stu-id="ecc50-120">This pointer can point to a value of zero or the following value.</span></span>



| <span data-ttu-id="ecc50-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ecc50-121">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="ecc50-122">Значение</span><span class="sxs-lookup"><span data-stu-id="ecc50-122">Meaning</span></span>                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="RKEYSVC_CONNECT_SECURE_ONLY"></span><span id="rkeysvc_connect_secure_only"></span><dl> <span data-ttu-id="ecc50-123"><dt>**Ркэйсвк \_ \_ \_ только безопасное подключение**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="ecc50-123"><dt>**RKEYSVC\_CONNECT\_SECURE\_ONLY**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="ecc50-124">Клиент требует взаимной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ecc50-124">The client requires mutual authentication.</span></span> <span data-ttu-id="ecc50-125">Если это значение указано, откат к NTLM завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ecc50-125">If this value is specified, fallback to NTLM will fail.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ecc50-126">*сохраняется* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ecc50-126">*pReserved* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecc50-127">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="ecc50-127">Reserved.</span></span> <span data-ttu-id="ecc50-128">Присвойте этому параметру значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ecc50-128">Set this value to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ecc50-129">*фкэйсвккли* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ecc50-129">*phKeySvcCli* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecc50-130">Указатель на [**\_ обработчик кэйсвкк**](keysvcc-handle.md) , который получает открытый маркер службы ключа.</span><span class="sxs-lookup"><span data-stu-id="ecc50-130">A pointer to a [**KEYSVCC\_HANDLE**](keysvcc-handle.md) that receives the opened key service handle.</span></span> <span data-ttu-id="ecc50-131">По завершении использования маркера Освободите ресурс, вызвав функцию [**ркэйклосекэйсервице**](rkeyclosekeyservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ecc50-131">When you have finished using the handle, free the resource by calling the [**RKeyCloseKeyService**](rkeyclosekeyservice.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecc50-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ecc50-132">Return value</span></span>

<span data-ttu-id="ecc50-133">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ecc50-133">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="ecc50-134">Если функция завершается ошибкой, возвращается значение типа **ulong** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="ecc50-134">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecc50-135">Требования</span><span class="sxs-lookup"><span data-stu-id="ecc50-135">Requirements</span></span>



| <span data-ttu-id="ecc50-136">Требование</span><span class="sxs-lookup"><span data-stu-id="ecc50-136">Requirement</span></span> | <span data-ttu-id="ecc50-137">Значение</span><span class="sxs-lookup"><span data-stu-id="ecc50-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc50-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ecc50-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ecc50-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ecc50-139">None supported</span></span><br/>                                                             |
| <span data-ttu-id="ecc50-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ecc50-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ecc50-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ecc50-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ecc50-142">Header</span><span class="sxs-lookup"><span data-stu-id="ecc50-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecc50-143"><dt>Ркэйсвкк. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecc50-143"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecc50-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecc50-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecc50-145">**ркэйклосекэйсервице**</span><span class="sxs-lookup"><span data-stu-id="ecc50-145">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="ecc50-146">**ркэйпфксинсталл**</span><span class="sxs-lookup"><span data-stu-id="ecc50-146">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> </dl>

 

 




