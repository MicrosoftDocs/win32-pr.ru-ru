---
title: Метод SetEncryptionLevel класса Win32_TSGeneralSetting
description: Метод Сетенкриптионлевел задает уровень шифрования.
ms.assetid: 1822c4dc-bce6-489f-b21e-f96faffd2fa5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетенкриптионлевел
- Службы удаленных рабочих столов метода Сетенкриптионлевел, класс Win32_TSGeneralSetting
- Класс Win32_TSGeneralSetting службы удаленных рабочих столов, метод Сетенкриптионлевел
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetEncryptionLevel
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1fbe727c75851bb13252d196e1fe7d599f881c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136510"
---
# <a name="setencryptionlevel-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="73a53-106">Метод Сетенкриптионлевел \_ класса Win32 тсженералсеттинг</span><span class="sxs-lookup"><span data-stu-id="73a53-106">SetEncryptionLevel method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="73a53-107">Метод **сетенкриптионлевел** задает уровень шифрования.</span><span class="sxs-lookup"><span data-stu-id="73a53-107">The **SetEncryptionLevel** method sets the encryption level.</span></span>

## <a name="syntax"></a><span data-ttu-id="73a53-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73a53-108">Syntax</span></span>


```mof
uint32 SetEncryptionLevel(
  [in] uint32 MinEncryptionLevel
);
```



## <a name="parameters"></a><span data-ttu-id="73a53-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="73a53-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73a53-110">*Миненкриптионлевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73a53-110">*MinEncryptionLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73a53-111">Устанавливаемый минимальный уровень шифрования.</span><span class="sxs-lookup"><span data-stu-id="73a53-111">The minimum encryption level to set.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="73a53-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="73a53-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="73a53-113">Низкий уровень шифрования.</span><span class="sxs-lookup"><span data-stu-id="73a53-113">Low level of encryption.</span></span> <span data-ttu-id="73a53-114">С помощью 56-разрядного шифрования шифруются только данные, отправленные с клиента на сервер.</span><span class="sxs-lookup"><span data-stu-id="73a53-114">Only data sent from the client to the server is encrypted using 56-bit encryption.</span></span> <span data-ttu-id="73a53-115">Обратите внимание, что данные, отправленные с сервера клиенту, не шифруются.</span><span class="sxs-lookup"><span data-stu-id="73a53-115">Note that data sent from the server to the client is not encrypted.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="73a53-116"><span id="2"></span>**открыт**</span><span class="sxs-lookup"><span data-stu-id="73a53-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="73a53-117">Уровень шифрования, совместимый с клиентом.</span><span class="sxs-lookup"><span data-stu-id="73a53-117">Client-compatible level of encryption.</span></span> <span data-ttu-id="73a53-118">Все данные, отправляемые от клиента серверу и от сервера к клиенту, шифруются по максимальному ключу, поддерживаемому клиентом.</span><span class="sxs-lookup"><span data-stu-id="73a53-118">All data sent from client to server and from server to client is encrypted at the maximum key strength supported by the client.</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="73a53-119"><span id="3"></span>**3-5**</span><span class="sxs-lookup"><span data-stu-id="73a53-119"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="73a53-120">Высокий уровень шифрования.</span><span class="sxs-lookup"><span data-stu-id="73a53-120">High level of encryption.</span></span> <span data-ttu-id="73a53-121">Все данные, отправленные с клиента на сервер и с сервера на клиент, шифруются с помощью надежного 128-разрядного шифрования.</span><span class="sxs-lookup"><span data-stu-id="73a53-121">All data sent from client to server and from server to client is encrypted using strong 128-bit encryption.</span></span> <span data-ttu-id="73a53-122">Клиенты, не поддерживающие этот уровень шифрования, не могут подключиться.</span><span class="sxs-lookup"><span data-stu-id="73a53-122">Clients that do not support this level of encryption cannot connect.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="73a53-123"><span id="4"></span>**четырех**</span><span class="sxs-lookup"><span data-stu-id="73a53-123"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="73a53-124">Шифрование, совместимое с FIPS.</span><span class="sxs-lookup"><span data-stu-id="73a53-124">FIPS-compliant encryption.</span></span> <span data-ttu-id="73a53-125">Все данные, отправляемые от клиента серверу и от сервера к клиенту, шифруются и расшифровываются с помощью алгоритмов шифрования FIPS, использующих криптографические модули (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="73a53-125">All data sent from client to server and from server to client is encrypted and decrypted with the Federal Information Processing Standard (FIPS) encryption algorithms using the Microsoft cryptographic modules.</span></span> <span data-ttu-id="73a53-126">FIPS — это стандартное право «требования безопасности для криптографических модулей».</span><span class="sxs-lookup"><span data-stu-id="73a53-126">FIPS is a standard entitled "Security Requirements for Cryptographic Modules".</span></span> <span data-ttu-id="73a53-127">FIPS 140-1 (1994) и FIPS 140-2 (2001) описывают требования правительства для аппаратных и программных криптографических модулей, используемых в правительственных учреждениях США.</span><span class="sxs-lookup"><span data-stu-id="73a53-127">FIPS 140-1 (1994) and FIPS 140-2 (2001) describe government requirements for hardware and software cryptographic modules used within the U.S. government.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73a53-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73a53-128">Return value</span></span>

<span data-ttu-id="73a53-129">Возвращает успешное завершение, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="73a53-129">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="73a53-130">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="73a53-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="73a53-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73a53-131">Remarks</span></span>

<span data-ttu-id="73a53-132">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="73a53-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="73a53-133">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="73a53-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="73a53-134">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="73a53-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="73a53-135">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="73a53-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="73a53-136">Требования</span><span class="sxs-lookup"><span data-stu-id="73a53-136">Requirements</span></span>



| <span data-ttu-id="73a53-137">Требование</span><span class="sxs-lookup"><span data-stu-id="73a53-137">Requirement</span></span> | <span data-ttu-id="73a53-138">Значение</span><span class="sxs-lookup"><span data-stu-id="73a53-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73a53-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73a53-139">Minimum supported client</span></span><br/> | <span data-ttu-id="73a53-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73a53-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="73a53-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73a53-141">Minimum supported server</span></span><br/> | <span data-ttu-id="73a53-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73a53-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="73a53-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="73a53-143">Namespace</span></span><br/>                | <span data-ttu-id="73a53-144">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="73a53-144">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="73a53-145">MOF</span><span class="sxs-lookup"><span data-stu-id="73a53-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73a53-146"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73a53-146"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="73a53-147">DLL</span><span class="sxs-lookup"><span data-stu-id="73a53-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73a53-148"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73a53-148"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73a53-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73a53-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73a53-150">**\_Тсженералсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="73a53-150">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> </dl>

 

