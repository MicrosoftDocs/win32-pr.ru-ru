---
title: Метод Сетцертификате класса Win32_TSGatewayServerSettings
description: Задает хэш сертификата для привязки HTTPS через порт 443 в IIS.
ms.assetid: b5f794bc-17b1-401a-92d8-c9bbe5d0d05f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетцертификате
- Службы удаленных рабочих столов метода Сетцертификате, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Сетцертификате
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1da7e3abcca671b0c8bf70461c77d56e68cf68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137343"
---
# <a name="setcertificate-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="c4f87-106">Метод Сетцертификате \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="c4f87-106">SetCertificate method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="c4f87-107">Задает хэш сертификата для привязки HTTPS через порт 443 в IIS.</span><span class="sxs-lookup"><span data-stu-id="c4f87-107">Sets the certificate hash for HTTPS binding on port 443 in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4f87-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4f87-108">Syntax</span></span>


```mof
uint32 SetCertificate(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="c4f87-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4f87-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4f87-110">*CertHash* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4f87-110">*CertHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4f87-111">Тип: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="c4f87-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="c4f87-112">Новый хэш сертификата.</span><span class="sxs-lookup"><span data-stu-id="c4f87-112">The new certificate hash.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4f87-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4f87-113">Return value</span></span>

<span data-ttu-id="c4f87-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c4f87-114">Type: **uint32**</span></span>

<span data-ttu-id="c4f87-115">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="c4f87-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c4f87-116">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="c4f87-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c4f87-117">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c4f87-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c4f87-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c4f87-118">Remarks</span></span>

<span data-ttu-id="c4f87-119">После того как хэш сертификата будет установлен с помощью этого метода, необходимо вызвать метод [**Configure**](configure-win32-tsgatewayserversettings.md) , чтобы завершить процесс настройки.</span><span class="sxs-lookup"><span data-stu-id="c4f87-119">After the certificate hash has been set with this method, you must call the [**Configure**](configure-win32-tsgatewayserversettings.md) method to complete the configuration process.</span></span>

<span data-ttu-id="c4f87-120">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="c4f87-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c4f87-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="c4f87-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c4f87-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="c4f87-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c4f87-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="c4f87-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c4f87-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c4f87-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4f87-125">Требования</span><span class="sxs-lookup"><span data-stu-id="c4f87-125">Requirements</span></span>



| <span data-ttu-id="c4f87-126">Требование</span><span class="sxs-lookup"><span data-stu-id="c4f87-126">Requirement</span></span> | <span data-ttu-id="c4f87-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c4f87-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4f87-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4f87-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c4f87-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c4f87-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c4f87-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4f87-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c4f87-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c4f87-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="c4f87-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c4f87-132">Namespace</span></span><br/>                | <span data-ttu-id="c4f87-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="c4f87-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c4f87-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c4f87-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4f87-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4f87-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4f87-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c4f87-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4f87-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4f87-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c4f87-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4f87-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4f87-139">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="c4f87-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

