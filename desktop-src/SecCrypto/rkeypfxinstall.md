---
description: Функция Ркэйпфксинсталл не поддерживается.
ms.assetid: 061e3d9d-fc92-4204-92f3-f3425afdbe27
title: Функция Ркэйпфксинсталл (Ркэйсвкк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyPFXInstall
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 4908b7224a02f5a28b876b1ff67cbcec7d23df5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991132"
---
# <a name="rkeypfxinstall-function"></a><span data-ttu-id="4fe08-103">Функция Ркэйпфксинсталл</span><span class="sxs-lookup"><span data-stu-id="4fe08-103">RKeyPFXInstall function</span></span>

<span data-ttu-id="4fe08-104">Функция **ркэйпфксинсталл** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4fe08-104">The **RKeyPFXInstall** function is not supported.</span></span>

<span data-ttu-id="4fe08-105">**Windows Server 2003:** Функция **ркэйпфксинсталл** устанавливает сертификат на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4fe08-105">**Windows Server 2003:** The **RKeyPFXInstall** function installs a certificate on a remote computer.</span></span> <span data-ttu-id="4fe08-106">Обратите внимание, что это поведение изменилось в Windows Server 2003 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4fe08-106">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="4fe08-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fe08-107">Syntax</span></span>


```C++
ULONG RKeyPFXInstall(
  _In_ KEYSVCC_HANDLE         hKeySvcCli,
  _In_ PKEYSVC_BLOB           pPFX,
  _In_ PKEYSVC_UNICODE_STRING pPassword,
  _In_ ULONG                  ulFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4fe08-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4fe08-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fe08-109">*хкэйсвккли* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4fe08-109">*hKeySvcCli* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe08-110">Обработчик [**\_ обработчика кэйсвкк**](keysvcc-handle.md) , который ранее открывался [**ркэйопенкэйсервице**](rkeyopenkeyservice.md).</span><span class="sxs-lookup"><span data-stu-id="4fe08-110">A [**KEYSVCC\_HANDLE**](keysvcc-handle.md) handle previously opened by [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span></span> <span data-ttu-id="4fe08-111">Этот маркер представляет удаленный компьютер, который получит сертификат.</span><span class="sxs-lookup"><span data-stu-id="4fe08-111">The handle represents the remote computer that will receive the certificate.</span></span> <span data-ttu-id="4fe08-112">Это значение не может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="4fe08-112">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4fe08-113">*ппфкс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4fe08-113">*pPFX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe08-114">Указатель на структуру [**\_ больших двоичных объектов кэйсвк**](keysvc-blob.md) , представляющую устанавливаемый сертификат.</span><span class="sxs-lookup"><span data-stu-id="4fe08-114">A pointer to a [**KEYSVC\_BLOB**](keysvc-blob.md) structure that represents the certificate to install.</span></span> <span data-ttu-id="4fe08-115">Большой двоичный объект находится в формате [*PKCS \# 12*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="4fe08-115">The BLOB is in [*PKCS \#12*](../secgloss/p-gly.md) format.</span></span>

</dd> <dt>

<span data-ttu-id="4fe08-116">*ппассворд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4fe08-116">*pPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe08-117">Указатель на структуру [**\_ \_ строки Юникода кэйсвк**](keysvc-unicode-string.md) , которая представляет пароль для большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="4fe08-117">A pointer to a [**KEYSVC\_UNICODE\_STRING**](keysvc-unicode-string.md) structure that represents the password for the BLOB.</span></span> <span data-ttu-id="4fe08-118">Завершив использование пароля, очистите его из памяти, вызвав функцию [**секурезеромемори**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4fe08-118">When you have finished using the password, clear the password from memory by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function.</span></span> <span data-ttu-id="4fe08-119">Дополнительные сведения о защите паролей см. в разделе [обработка паролей](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="4fe08-119">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="4fe08-120">*улфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4fe08-120">*ulFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe08-121">Флаги, указывающие параметры установки сертификата.</span><span class="sxs-lookup"><span data-stu-id="4fe08-121">Flags that specify the certificate installation options.</span></span> <span data-ttu-id="4fe08-122">Этот параметр может быть нулем или сочетанием следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4fe08-122">This parameter can be a zero or a combination of the following values.</span></span>



| <span data-ttu-id="4fe08-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4fe08-123">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="4fe08-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4fe08-124">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CRYPT_EXPORTABLE"></span><span id="crypt_exportable"></span><dl> <span data-ttu-id="4fe08-125"><dt>**Шифрования \_ Возможность экспорта**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="4fe08-125"><dt>**CRYPT\_EXPORTABLE**</dt> <dt></dt></span></span> </dl>              | <span data-ttu-id="4fe08-126">Импортированные ключи помечаются как доступные для экспорта.</span><span class="sxs-lookup"><span data-stu-id="4fe08-126">Imported keys are marked as exportable.</span></span><br/>                                           |
| <span id="CRYPT_MACHINE_KEYSET"></span><span id="crypt_machine_keyset"></span><dl> <span data-ttu-id="4fe08-127"><dt>**Шифрования \_ \_набор ключей компьютера**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="4fe08-127"><dt>**CRYPT\_MACHINE\_KEYSET**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="4fe08-128">Закрытые ключи хранятся на удаленном компьютере, а не в текущем пользователе.</span><span class="sxs-lookup"><span data-stu-id="4fe08-128">Private keys are stored under the remote computer and not under the current user.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fe08-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4fe08-129">Return value</span></span>

<span data-ttu-id="4fe08-130">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4fe08-130">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="4fe08-131">Если функция завершается ошибкой, возвращается значение типа **ulong** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="4fe08-131">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fe08-132">Требования</span><span class="sxs-lookup"><span data-stu-id="4fe08-132">Requirements</span></span>



| <span data-ttu-id="4fe08-133">Требование</span><span class="sxs-lookup"><span data-stu-id="4fe08-133">Requirement</span></span> | <span data-ttu-id="4fe08-134">Значение</span><span class="sxs-lookup"><span data-stu-id="4fe08-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4fe08-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fe08-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4fe08-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4fe08-136">None supported</span></span><br/>                                                             |
| <span data-ttu-id="4fe08-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fe08-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4fe08-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4fe08-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4fe08-139">Header</span><span class="sxs-lookup"><span data-stu-id="4fe08-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fe08-140"><dt>Ркэйсвкк. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fe08-140"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fe08-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fe08-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fe08-142">**ркэйклосекэйсервице**</span><span class="sxs-lookup"><span data-stu-id="4fe08-142">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="4fe08-143">**ркэйопенкэйсервице**</span><span class="sxs-lookup"><span data-stu-id="4fe08-143">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 
