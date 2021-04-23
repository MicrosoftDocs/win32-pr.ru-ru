---
title: IMsRdpClientNonScriptable5 Ремотемониторлайаутматчеслокал, свойство
description: Указывает, идентичен ли макет удаленного монитора структуре локального монитора.
ms.assetid: 8F3C6650-870C-417C-82FC-E145FC360012
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Ремотемониторлайаутматчеслокал
- Службы удаленных рабочих столов свойства Ремотемониторлайаутматчеслокал, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Ремотемониторлайаутматчеслокал
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.RemoteMonitorLayoutMatchesLocal
- IMsRdpClientNonScriptable5.get_RemoteMonitorLayoutMatchesLocal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5018b22865cc683fc9231c857a1b99b8acbfeca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136526"
---
# <a name="imsrdpclientnonscriptable5remotemonitorlayoutmatcheslocal-property"></a><span data-ttu-id="a9462-106">Свойство IMsRdpClientNonScriptable5:: Ремотемониторлайаутматчеслокал</span><span class="sxs-lookup"><span data-stu-id="a9462-106">IMsRdpClientNonScriptable5::RemoteMonitorLayoutMatchesLocal property</span></span>

<span data-ttu-id="a9462-107">Указывает, идентичен ли макет удаленного монитора структуре локального монитора.</span><span class="sxs-lookup"><span data-stu-id="a9462-107">Specifies if the remote monitor layout is identical to the local monitor layout.</span></span> <span data-ttu-id="a9462-108">Если это свойство содержит **вариант \_ true**, макет удаленного монитора идентичен макету локального монитора.</span><span class="sxs-lookup"><span data-stu-id="a9462-108">If this property contains **VARIANT\_TRUE**, the remote monitor layout is identical to the local monitor layout.</span></span> <span data-ttu-id="a9462-109">Если это свойство содержит **вариант \_ false**, то удаленный и локальный мониторы имеют разные макеты.</span><span class="sxs-lookup"><span data-stu-id="a9462-109">If this property contains **VARIANT\_FALSE**, the remote and local monitors have different layouts.</span></span>

<span data-ttu-id="a9462-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a9462-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9462-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9462-111">Syntax</span></span>


```C++
HRESULT get_RemoteMonitorLayoutMatchesLocal(
  [out, retval] VARIANT_BOOL *pfRemoteMatchesLocal
);
```



## <a name="property-value"></a><span data-ttu-id="a9462-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a9462-112">Property value</span></span>

<span data-ttu-id="a9462-113">Получает значение свойства.</span><span class="sxs-lookup"><span data-stu-id="a9462-113">Receives the property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9462-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a9462-114">Requirements</span></span>



| <span data-ttu-id="a9462-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a9462-115">Requirement</span></span> | <span data-ttu-id="a9462-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a9462-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9462-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9462-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a9462-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9462-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a9462-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9462-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a9462-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a9462-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="a9462-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a9462-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="a9462-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9462-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="a9462-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a9462-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9462-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9462-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="a9462-125">IID</span><span class="sxs-lookup"><span data-stu-id="a9462-125">IID</span></span><br/>                      | <span data-ttu-id="a9462-126">IID \_ IMsRdpClientNonScriptable5 определен как 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="a9462-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a9462-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9462-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9462-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="a9462-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





