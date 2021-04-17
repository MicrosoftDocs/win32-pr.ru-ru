---
title: Итспубплугин pluginName, свойство
description: Возвращает имя подключаемого модуля.
ms.assetid: c1ea46b6-fac6-4140-a278-cb04ee9af739
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства pluginName
- службы удаленных рабочих столов свойства pluginName, интерфейс Итспубплугин
- Службы удаленных рабочих столов интерфейса Итспубплугин, свойство pluginName
topic_type:
- apiref
api_name:
- ItsPubPlugin.pluginName
- ItsPubPlugin.get_pluginName
api_location:
- Cpubplugin.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f5aa6ff6659047e9be48fd7b7a41f652c5cfd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681966"
---
# <a name="itspubpluginpluginname-property"></a><span data-ttu-id="65c8e-106">Итспубплугин: свойство Лугиннаме:p</span><span class="sxs-lookup"><span data-stu-id="65c8e-106">ItsPubPlugin::pluginName property</span></span>

<span data-ttu-id="65c8e-107">Возвращает имя подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="65c8e-107">Retrieves the name of the plug-in.</span></span>

<span data-ttu-id="65c8e-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="65c8e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="65c8e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65c8e-109">Syntax</span></span>


```C++
HRESULT get_pluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="65c8e-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="65c8e-110">Property value</span></span>

<span data-ttu-id="65c8e-111">Указатель на переменную **BSTR** , чтобы получить имя подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="65c8e-111">A pointer to a **BSTR** variable to receive the name of the plug-in.</span></span>

## <a name="requirements"></a><span data-ttu-id="65c8e-112">Требования</span><span class="sxs-lookup"><span data-stu-id="65c8e-112">Requirements</span></span>



| <span data-ttu-id="65c8e-113">Требование</span><span class="sxs-lookup"><span data-stu-id="65c8e-113">Requirement</span></span> | <span data-ttu-id="65c8e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="65c8e-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="65c8e-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65c8e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="65c8e-116">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="65c8e-116">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="65c8e-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65c8e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="65c8e-118">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="65c8e-118">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="65c8e-119">IDL</span><span class="sxs-lookup"><span data-stu-id="65c8e-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="65c8e-120"><dt>Кпубплугин. idl</dt></span><span class="sxs-lookup"><span data-stu-id="65c8e-120"><dt>Cpubplugin.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65c8e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65c8e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65c8e-122">**итспубплугин**</span><span class="sxs-lookup"><span data-stu-id="65c8e-122">**ItsPubPlugin**</span></span>](/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin)
</dt> </dl>

 

 





