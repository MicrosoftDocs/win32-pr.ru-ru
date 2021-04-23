---
description: Использует указанную строку идентификатора безопасности (SID) Active Directory для получения производного ключа и разблокировки зашифрованного тома.
ms.assetid: 89FBC815-859D-415A-8F26-170FB2DB7387
title: Метод Унлокквисадсид класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: cbd2a327a2ede322c01009fe32aa0492a7e65610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664381"
---
# <a name="unlockwithadsid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="fb401-103">Метод Унлокквисадсид \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="fb401-103">UnlockWithAdSid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="fb401-104">Метод **унлокквисадсид** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) использует указанную строку идентификатора безопасности Active Directory, чтобы получить производный ключ и разблокировать зашифрованный том.</span><span class="sxs-lookup"><span data-stu-id="fb401-104">The **UnlockWithAdSid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided Active Directory security identifier (SID) string to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="fb401-105">Если диск поддерживает аппаратное шифрование, эта функция устанавливает для полосы состояние "разблокирован".</span><span class="sxs-lookup"><span data-stu-id="fb401-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fb401-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb401-106">Syntax</span></span>


```mof
uint32 UnlockWithAdSid(
  [in]  string SidString
);
```



## <a name="parameters"></a><span data-ttu-id="fb401-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb401-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb401-108">*Сидстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fb401-108">*SidString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb401-109">Строка, содержащая идентификатор безопасности Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fb401-109">String that contains the Active Directory SID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb401-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb401-110">Return value</span></span>

<span data-ttu-id="fb401-111">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="fb401-111">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="fb401-112">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="fb401-112">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="fb401-113">Описание</span><span class="sxs-lookup"><span data-stu-id="fb401-113">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="fb401-114"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="fb401-114"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="fb401-115">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="fb401-115">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fb401-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb401-116">Remarks</span></span>

<span data-ttu-id="fb401-117">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="fb401-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fb401-118">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="fb401-118">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="fb401-119">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="fb401-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fb401-120">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="fb401-120">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb401-121">Требования</span><span class="sxs-lookup"><span data-stu-id="fb401-121">Requirements</span></span>



| <span data-ttu-id="fb401-122">Требование</span><span class="sxs-lookup"><span data-stu-id="fb401-122">Requirement</span></span> | <span data-ttu-id="fb401-123">Значение</span><span class="sxs-lookup"><span data-stu-id="fb401-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb401-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb401-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fb401-125">Windows 8 Корпоративная, \[ только классические приложения Windows 8 Pro\]</span><span class="sxs-lookup"><span data-stu-id="fb401-125">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fb401-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb401-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fb401-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fb401-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb401-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fb401-128">Namespace</span></span><br/>                | <span data-ttu-id="fb401-129">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="fb401-129">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="fb401-130">MOF</span><span class="sxs-lookup"><span data-stu-id="fb401-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb401-131"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb401-131"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb401-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb401-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb401-133">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="fb401-133">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
