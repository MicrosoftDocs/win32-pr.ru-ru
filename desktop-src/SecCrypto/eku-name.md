---
description: Задает или получает значение перечисления, которое указывает CAPICOM имя EKU. Это свойство по умолчанию.
ms.assetid: afce5553-ef18-4a7f-b1c8-fbe00d3277e0
title: 'Свойство ИЕКУ:: Name'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.Name
- IEKU.get_Name
- IEKU.put_Name
- EKU.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0e28a8816d7e4c4f44e3cd1ec0dc479372d66d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648909"
---
# <a name="iekuname-property"></a><span data-ttu-id="f3b2a-104">Свойство ИЕКУ:: Name</span><span class="sxs-lookup"><span data-stu-id="f3b2a-104">IEKU::Name property</span></span>

<span data-ttu-id="f3b2a-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f3b2a-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f3b2a-106">Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f3b2a-106">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f3b2a-107">Свойство **Name** задает или получает значение перечисления, которое указывает CAPICOM Name EKU.</span><span class="sxs-lookup"><span data-stu-id="f3b2a-107">The **Name** property sets or retrieves an enumeration value that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="f3b2a-108">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3b2a-108">This is the default property.</span></span>

<span data-ttu-id="f3b2a-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f3b2a-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b2a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3b2a-110">Syntax</span></span>


```VB
EKU.Name As CAPICOM_EKU
```



## <a name="property-value"></a><span data-ttu-id="f3b2a-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f3b2a-111">Property value</span></span>

<span data-ttu-id="f3b2a-112">Значение перечисления [**CAPICOM \_ EKU**](capicom-eku.md) , которое указывает CAPICOM-имя EKU.</span><span class="sxs-lookup"><span data-stu-id="f3b2a-112">A value of the [**CAPICOM\_EKU**](capicom-eku.md) enumeration that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="f3b2a-113">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="f3b2a-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="f3b2a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f3b2a-114">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="f3b2a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f3b2a-115">Meaning</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_EKU_OTHER"></span><span id="capicom_eku_other"></span><dl> <span data-ttu-id="f3b2a-116"><dt>**\_другое расширенное EKU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f3b2a-116"><dt>**CAPICOM\_EKU\_OTHER**</dt></span></span> </dl>                                                      | <span data-ttu-id="f3b2a-117">В сертификате используются определенные в локальной политике.</span><span class="sxs-lookup"><span data-stu-id="f3b2a-117">Certificate has uses defined in local policy.</span></span> <span data-ttu-id="f3b2a-118">Используется, если требуемое EKU не определено и значение OID должно быть задано приложением.</span><span class="sxs-lookup"><span data-stu-id="f3b2a-118">This is used if the EKU needed is not predefined and the OID value must be set by the application.</span></span><br/> |
| <span id="CAPICOM_EKU_SERVER_AUTH"></span><span id="capicom_eku_server_auth"></span><dl> <span data-ttu-id="f3b2a-119"><dt>**\_ \_ \_ Проверка подлинности сервера CAPICOM EKU**</dt></span><span class="sxs-lookup"><span data-stu-id="f3b2a-119"><dt>**CAPICOM\_EKU\_SERVER\_AUTH**</dt></span></span> </dl>                                   | <span data-ttu-id="f3b2a-120">Сертификат можно использовать для проверки подлинности сервера.</span><span class="sxs-lookup"><span data-stu-id="f3b2a-120">Certificate can be used to authenticate a server.</span></span><br/>                                                                                                |
| <span id="CAPICOM_EKU_CLIENT_AUTH"></span><span id="capicom_eku_client_auth"></span><dl> <span data-ttu-id="f3b2a-121"><dt>**\_ \_ \_ Проверка подлинности клиента CAPICOM EKU**</dt></span><span class="sxs-lookup"><span data-stu-id="f3b2a-121"><dt>**CAPICOM\_EKU\_CLIENT\_AUTH**</dt></span></span> </dl>                                   | <span data-ttu-id="f3b2a-122">Сертификат можно использовать для проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="f3b2a-122">Certificate can be used to authenticate a client.</span></span><br/>                                                                                                |
| <span id="CAPICOM_EKU_CODE_SIGNING"></span><span id="capicom_eku_code_signing"></span><dl> <span data-ttu-id="f3b2a-123"><dt>**\_Подписывание \_ кода CAPICOM EKU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f3b2a-123"><dt>**CAPICOM\_EKU\_CODE\_SIGNING**</dt></span></span> </dl>                                | <span data-ttu-id="f3b2a-124">Сертификат можно использовать для создания цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="f3b2a-124">Certificate can be used to create a digital signature.</span></span><br/>                                                                                           |
| <span id="CAPICOM_EKU_EMAIL_PROTECTION"></span><span id="capicom_eku_email_protection"></span><dl> <span data-ttu-id="f3b2a-125"><dt>**\_ \_ Защита электронной почты CAPICOM EKU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f3b2a-125"><dt>**CAPICOM\_EKU\_EMAIL\_PROTECTION**</dt></span></span> </dl>                    | <span data-ttu-id="f3b2a-126">Сертификат можно использовать для защиты электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f3b2a-126">Certificate can be used for email protection.</span></span><br/>                                                                                                    |
| <span id="CAPICOM_EKU_SMARTCARD_LOGON"></span><span id="capicom_eku_smartcard_logon"></span><dl> <span data-ttu-id="f3b2a-127"><dt>**\_Вход в \_ смарт-карту CAPICOM EKU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f3b2a-127"><dt>**CAPICOM\_EKU\_SMARTCARD\_LOGON**</dt></span></span> </dl>                       | <span data-ttu-id="f3b2a-128">Сертификат можно использовать для входа с использованием смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="f3b2a-128">Certificate can be used for smart card logon.</span></span> <span data-ttu-id="f3b2a-129">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="f3b2a-129">Introduced in CAPICOM 2.0.</span></span><br/>                                                                         |
| <span id="CAPICOM_EKU_ENCRYPTING_FILE_SYSTEM"></span><span id="capicom_eku_encrypting_file_system"></span><dl> <span data-ttu-id="f3b2a-130"><dt>**\_ \_ \_ Файловая система с шифрованием CAPICOM EKU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f3b2a-130"><dt>**CAPICOM\_EKU\_ENCRYPTING\_FILE\_SYSTEM**</dt></span></span> </dl> | <span data-ttu-id="f3b2a-131">Сертификат можно использовать для EFS.</span><span class="sxs-lookup"><span data-stu-id="f3b2a-131">Certificate can be used for EFS.</span></span> <span data-ttu-id="f3b2a-132">Представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="f3b2a-132">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="f3b2a-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3b2a-133">Remarks</span></span>

<span data-ttu-id="f3b2a-134">Когда значение этого свойства сбрасывается прямо или косвенно, полное [*состояние*](../secgloss/s-gly.md) объекта сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="f3b2a-134">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3b2a-135">Требования</span><span class="sxs-lookup"><span data-stu-id="f3b2a-135">Requirements</span></span>



| <span data-ttu-id="f3b2a-136">Требование</span><span class="sxs-lookup"><span data-stu-id="f3b2a-136">Requirement</span></span> | <span data-ttu-id="f3b2a-137">Значение</span><span class="sxs-lookup"><span data-stu-id="f3b2a-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b2a-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f3b2a-138">End of client support</span></span><br/> | <span data-ttu-id="f3b2a-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3b2a-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f3b2a-140">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f3b2a-140">End of server support</span></span><br/> | <span data-ttu-id="f3b2a-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3b2a-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f3b2a-142">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="f3b2a-142">Redistributable</span></span><br/>       | <span data-ttu-id="f3b2a-143">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="f3b2a-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f3b2a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f3b2a-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f3b2a-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3b2a-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
