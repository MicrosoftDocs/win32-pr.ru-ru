---
title: Метод Тсгстореконсентмсг класса Win32_TSGatewayServerSettings
description: Обновляет сообщение согласия для сервера шлюза.
ms.assetid: b3146d87-95af-4b6b-8c02-5ac4748fbe98
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Тсгстореконсентмсг
- Службы удаленных рабочих столов метода Тсгстореконсентмсг, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Тсгстореконсентмсг
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreConsentMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907097739d21e1523aca3b719cdb5f18b6f3fa30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490983"
---
# <a name="tsgstoreconsentmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="08fe0-106">Метод Тсгстореконсентмсг \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="08fe0-106">TSGStoreConsentMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="08fe0-107">Обновляет сообщение согласия для сервера шлюза.</span><span class="sxs-lookup"><span data-stu-id="08fe0-107">Updates the consent message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="08fe0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08fe0-108">Syntax</span></span>


```mof
uint32 TSGStoreConsentMsg(
  [in] string TSGConMsgText
);
```



## <a name="parameters"></a><span data-ttu-id="08fe0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="08fe0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08fe0-110">*Тсгконмсгтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08fe0-110">*TSGConMsgText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08fe0-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="08fe0-111">Type: **string**</span></span>

<span data-ttu-id="08fe0-112">Текст сообщения согласия.</span><span class="sxs-lookup"><span data-stu-id="08fe0-112">The consent message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08fe0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08fe0-113">Return value</span></span>

<span data-ttu-id="08fe0-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08fe0-114">Type: **uint32**</span></span>

<span data-ttu-id="08fe0-115">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="08fe0-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="08fe0-116">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="08fe0-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="08fe0-117">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="08fe0-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="08fe0-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08fe0-118">Remarks</span></span>

<span data-ttu-id="08fe0-119">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="08fe0-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="08fe0-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="08fe0-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="08fe0-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="08fe0-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="08fe0-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="08fe0-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="08fe0-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="08fe0-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="08fe0-124">Требования</span><span class="sxs-lookup"><span data-stu-id="08fe0-124">Requirements</span></span>



| <span data-ttu-id="08fe0-125">Требование</span><span class="sxs-lookup"><span data-stu-id="08fe0-125">Requirement</span></span> | <span data-ttu-id="08fe0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="08fe0-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="08fe0-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08fe0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="08fe0-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="08fe0-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="08fe0-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08fe0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="08fe0-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="08fe0-130">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="08fe0-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="08fe0-131">Namespace</span></span><br/>                | <span data-ttu-id="08fe0-132">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="08fe0-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="08fe0-133">MOF</span><span class="sxs-lookup"><span data-stu-id="08fe0-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08fe0-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08fe0-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="08fe0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="08fe0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08fe0-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08fe0-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="08fe0-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08fe0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08fe0-138">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="08fe0-138">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

