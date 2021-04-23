---
description: Выполняет самотестирование TPM и возвращает результат.
ms.assetid: 0f8fdb68-80b1-4fc4-beb9-e87f51b85031
title: Метод SelfTest класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.SelfTest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8681ee8ca49b8b2f7de550ffc5baa0ff8c0c9470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662288"
---
# <a name="selftest-method-of-the-win32_tpm-class"></a><span data-ttu-id="58f41-103">Метод SelfTest \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="58f41-103">SelfTest method of the Win32\_Tpm class</span></span>

<span data-ttu-id="58f41-104">Метод **SelfTest** класса [**\_ TPM Win32**](win32-tpm.md) выполняет самотестирование TPM и возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="58f41-104">The **SelfTest** method of the [**Win32\_Tpm**](win32-tpm.md) class performs a self-test of the TPM and returns the result.</span></span>

<span data-ttu-id="58f41-105">Самотест TPM запускается автоматически при запуске компьютера.</span><span class="sxs-lookup"><span data-stu-id="58f41-105">A TPM self-test runs automatically when the computer starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="58f41-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58f41-106">Syntax</span></span>


```mof
uint32 SelfTest(
  [out] uint8 SelfTestResult[]
);
```



## <a name="parameters"></a><span data-ttu-id="58f41-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="58f41-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58f41-108">*Селфтестресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="58f41-108">*SelfTestResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58f41-109">Тип: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="58f41-109">Type: **uint8\[\]**</span></span>

<span data-ttu-id="58f41-110">Массив байтов, содержащий результат самотестирования.</span><span class="sxs-lookup"><span data-stu-id="58f41-110">An array of bytes that contains the self-test result.</span></span> <span data-ttu-id="58f41-111">Этот параметр имеет формат, зависящий от производителя.</span><span class="sxs-lookup"><span data-stu-id="58f41-111">The format of this parameter is manufacturer-specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58f41-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58f41-112">Return value</span></span>

<span data-ttu-id="58f41-113">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58f41-113">Type: **uint32**</span></span>

<span data-ttu-id="58f41-114">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="58f41-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="58f41-115">В следующей таблице перечислены некоторые распространенные коды возврата.</span><span class="sxs-lookup"><span data-stu-id="58f41-115">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="58f41-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="58f41-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="58f41-117">Описание</span><span class="sxs-lookup"><span data-stu-id="58f41-117">Description</span></span>                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="58f41-118"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="58f41-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="58f41-119">Метод успешно запущен.</span><span class="sxs-lookup"><span data-stu-id="58f41-119">The method ran successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="58f41-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58f41-120">Remarks</span></span>

<span data-ttu-id="58f41-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="58f41-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="58f41-122">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="58f41-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="58f41-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="58f41-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="58f41-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="58f41-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="58f41-125">Требования</span><span class="sxs-lookup"><span data-stu-id="58f41-125">Requirements</span></span>



| <span data-ttu-id="58f41-126">Требование</span><span class="sxs-lookup"><span data-stu-id="58f41-126">Requirement</span></span> | <span data-ttu-id="58f41-127">Значение</span><span class="sxs-lookup"><span data-stu-id="58f41-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="58f41-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58f41-128">Minimum supported client</span></span><br/> | <span data-ttu-id="58f41-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58f41-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="58f41-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58f41-130">Minimum supported server</span></span><br/> | <span data-ttu-id="58f41-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="58f41-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="58f41-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="58f41-132">Namespace</span></span><br/>                | <span data-ttu-id="58f41-133">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="58f41-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="58f41-134">MOF</span><span class="sxs-lookup"><span data-stu-id="58f41-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58f41-135"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58f41-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="58f41-136">DLL</span><span class="sxs-lookup"><span data-stu-id="58f41-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58f41-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="58f41-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58f41-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58f41-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58f41-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="58f41-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
