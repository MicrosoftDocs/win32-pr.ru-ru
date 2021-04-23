---
title: Имсрдпклиентадванцедсеттингс Сассекуенце, свойство
description: Указывает последовательность безопасного доступа (SAS), которую клиент будет использовать для доступа к экрану входа на сервере.
ms.assetid: ec1dc7b1-2bf1-447b-a768-08f28982a995
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Сассекуенце
- Службы удаленных рабочих столов свойства Сассекуенце, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Сассекуенце
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SasSequence
- IMsRdpClientAdvancedSettings.get_SasSequence
- IMsRdpClientAdvancedSettings.put_SasSequence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf38a4e1f048e67613b92b3629aa96cca281b1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489126"
---
# <a name="imsrdpclientadvancedsettingssassequence-property"></a><span data-ttu-id="38643-106">Свойство Имсрдпклиентадванцедсеттингс:: Сассекуенце</span><span class="sxs-lookup"><span data-stu-id="38643-106">IMsRdpClientAdvancedSettings::SasSequence property</span></span>

<span data-ttu-id="38643-107">Указывает последовательность безопасного доступа (SAS), которую клиент будет использовать для доступа к экрану входа на сервере.</span><span class="sxs-lookup"><span data-stu-id="38643-107">Specifies the secure access sequence (SAS) the client will use to access the login screen on the server.</span></span>

<span data-ttu-id="38643-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="38643-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="38643-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38643-109">Syntax</span></span>


```C++
HRESULT put_SasSequence(
  [in]  LONG sasSequence
);

HRESULT get_SasSequence(
  [out] LONG *psasSequence
);
```



## <a name="property-value"></a><span data-ttu-id="38643-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="38643-110">Property value</span></span>

<span data-ttu-id="38643-111">Значение **типа Long** , содержащее индикатор SAS.</span><span class="sxs-lookup"><span data-stu-id="38643-111">A **LONG** value that contains the SAS indicator.</span></span> <span data-ttu-id="38643-112">Единственное поддерживаемое значение — 0xaa03, которое указывает стандартную последовательность CTRL + ALT + DELETE.</span><span class="sxs-lookup"><span data-stu-id="38643-112">The only supported value is 0xaa03, which indicates the standard CTRL+ALT+DELETE sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="38643-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38643-113">Remarks</span></span>

<span data-ttu-id="38643-114">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="38643-114">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38643-115">Требования</span><span class="sxs-lookup"><span data-stu-id="38643-115">Requirements</span></span>



| <span data-ttu-id="38643-116">Требование</span><span class="sxs-lookup"><span data-stu-id="38643-116">Requirement</span></span> | <span data-ttu-id="38643-117">Значение</span><span class="sxs-lookup"><span data-stu-id="38643-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38643-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38643-118">Minimum supported client</span></span><br/> | <span data-ttu-id="38643-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38643-119">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="38643-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38643-120">Minimum supported server</span></span><br/> | <span data-ttu-id="38643-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38643-121">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="38643-122">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="38643-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="38643-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38643-123"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="38643-124">DLL</span><span class="sxs-lookup"><span data-stu-id="38643-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38643-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38643-125"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="38643-126">IID</span><span class="sxs-lookup"><span data-stu-id="38643-126">IID</span></span><br/>                      | <span data-ttu-id="38643-127">IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="38643-127">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38643-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38643-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38643-129">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="38643-129">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





