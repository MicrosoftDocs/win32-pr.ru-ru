---
description: Создает 2048-разрядную пару ключей подтверждения в доверенном платформенном модуле.
ms.assetid: 393f0264-d1e9-4a08-bdaa-475b32d93e05
title: Метод Креатиндорсементкэйпаир класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.CreateEndorsementKeyPair
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5839dc009d8af420a91f2e7c925f2cac5567d2a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540946"
---
# <a name="createendorsementkeypair-method-of-the-win32_tpm-class"></a><span data-ttu-id="039f1-103">Метод Креатиндорсементкэйпаир \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="039f1-103">CreateEndorsementKeyPair method of the Win32\_Tpm class</span></span>

<span data-ttu-id="039f1-104">Метод **креатиндорсементкэйпаир** класса [**\_ Tpm Win32**](win32-tpm.md) создает пару 2048-битного ключа подтверждения в доверенном платформенном модуле.</span><span class="sxs-lookup"><span data-stu-id="039f1-104">The **CreateEndorsementKeyPair** method of the [**Win32\_Tpm**](win32-tpm.md) class creates an 2048-bit endorsement key pair on the TPM.</span></span> <span data-ttu-id="039f1-105">Для успешного выполнения метода [**такеовнершип**](takeownership-win32-tpm.md) должна быть доступна пара ключей подтверждения.</span><span class="sxs-lookup"><span data-stu-id="039f1-105">The endorsement key pair must be available for the [**TakeOwnership**](takeownership-win32-tpm.md) method to run successfully.</span></span> <span data-ttu-id="039f1-106">С помощью метода [**исендорсементкэйпаирпресент**](isendorsementkeypairpresent-win32-tpm.md) можно определить, существует ли уже ключ подтверждения в доверенном платформенном модуле.</span><span class="sxs-lookup"><span data-stu-id="039f1-106">You can use the [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) method to detect whether the endorsement key already exists on the TPM.</span></span>

## <a name="syntax"></a><span data-ttu-id="039f1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="039f1-107">Syntax</span></span>


```mof
uint32 CreateEndorsementKeyPair();
```



## <a name="parameters"></a><span data-ttu-id="039f1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="039f1-108">Parameters</span></span>

<span data-ttu-id="039f1-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="039f1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="039f1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="039f1-110">Return value</span></span>

<span data-ttu-id="039f1-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="039f1-111">Type: **uint32**</span></span>

<span data-ttu-id="039f1-112">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="039f1-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="039f1-113">В следующей таблице перечислены некоторые распространенные коды возврата.</span><span class="sxs-lookup"><span data-stu-id="039f1-113">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="039f1-114">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="039f1-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="039f1-115">Описание</span><span class="sxs-lookup"><span data-stu-id="039f1-115">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="039f1-116"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="039f1-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="039f1-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="039f1-117">The method was successful.</span></span><br/>                          |
| <dl> <span data-ttu-id="039f1-118"><dt> **TPM \_ E \_ отключил \_ cmd-командлет**</dt> <dt>2150105096 (0x80280008)</dt></span><span class="sxs-lookup"><span data-stu-id="039f1-118"><dt>**TPM\_E\_DISABLED\_CMD** </dt> <dt>2150105096 (0x80280008)</dt></span></span> </dl> | <span data-ttu-id="039f1-119">Пара ключей подтверждения уже существует в этом доверенном платформенном модуле.</span><span class="sxs-lookup"><span data-stu-id="039f1-119">An endorsement key pair already exists on this TPM.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="039f1-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="039f1-120">Remarks</span></span>

<span data-ttu-id="039f1-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="039f1-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="039f1-122">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="039f1-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="039f1-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="039f1-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="039f1-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="039f1-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="039f1-125">Требования</span><span class="sxs-lookup"><span data-stu-id="039f1-125">Requirements</span></span>



| <span data-ttu-id="039f1-126">Требование</span><span class="sxs-lookup"><span data-stu-id="039f1-126">Requirement</span></span> | <span data-ttu-id="039f1-127">Значение</span><span class="sxs-lookup"><span data-stu-id="039f1-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="039f1-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="039f1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="039f1-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="039f1-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="039f1-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="039f1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="039f1-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="039f1-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="039f1-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="039f1-132">Namespace</span></span><br/>                | <span data-ttu-id="039f1-133">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="039f1-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="039f1-134">MOF</span><span class="sxs-lookup"><span data-stu-id="039f1-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="039f1-135"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="039f1-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="039f1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="039f1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="039f1-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="039f1-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="039f1-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="039f1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="039f1-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="039f1-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
