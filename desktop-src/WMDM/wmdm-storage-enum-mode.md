---
title: Перечисление WMDM_STORAGE_ENUM_MODE
description: '\_Тип перечисления "режим перечисления хранилища вмдм" \_ \_ определяет способ перечисления содержимого в хранилище. Это перечисление используется IWMDMStorage3 Сетенумпреференце.'
ms.assetid: 38293e54-92e4-4f0a-bdea-5dc684a9548b
keywords:
- WMDM_STORAGE_ENUM_MODE перечисление Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDM_STORAGE_ENUM_MODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d886ade00289e655ae3323a70d01be96a09852b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694548"
---
# <a name="wmdm_storage_enum_mode-enumeration"></a><span data-ttu-id="c32ed-105">\_ \_ Перечисление режима перечисления вмдм в хранилище \_</span><span class="sxs-lookup"><span data-stu-id="c32ed-105">WMDM\_STORAGE\_ENUM\_MODE enumeration</span></span>

<span data-ttu-id="c32ed-106">Тип перечисления " **\_ \_ \_ режим перечисления хранилища вмдм** " определяет способ перечисления содержимого в хранилище.</span><span class="sxs-lookup"><span data-stu-id="c32ed-106">The **WMDM\_STORAGE\_ENUM\_MODE** enumeration type defines how the content on the storage is to be enumerated.</span></span> <span data-ttu-id="c32ed-107">Это перечисление используется [**IWMDMStorage3:: сетенумпреференце**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference).</span><span class="sxs-lookup"><span data-stu-id="c32ed-107">This enumeration is used by [**IWMDMStorage3::SetEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setenumpreference).</span></span>

## <a name="syntax"></a><span data-ttu-id="c32ed-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c32ed-108">Syntax</span></span>


```C++
typedef enum tagWMDM_STORAGE_ENUM_MODE { 
  ENUM_MODE_RAW,
  ENUM_MODE_USE_DEVICE_PREF,
  ENUM_MODE_METADATA_VIEWS
} WMDM_STORAGE_ENUM_MODE;
```



## <a name="constants"></a><span data-ttu-id="c32ed-109">Константы</span><span class="sxs-lookup"><span data-stu-id="c32ed-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c32ed-110"><span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**\_режим перечисления \_ RAW**</span><span class="sxs-lookup"><span data-stu-id="c32ed-110"><span id="ENUM_MODE_RAW"></span><span id="enum_mode_raw"></span>**ENUM\_MODE\_RAW**</span></span>
</dt> <dd>

<span data-ttu-id="c32ed-111">Перечисляет содержимое в хранилище так же, как оно организовано в файловой системе хранилища.</span><span class="sxs-lookup"><span data-stu-id="c32ed-111">Enumerates content on the storage just as it is organized in the file system of the storage.</span></span>

<span data-ttu-id="c32ed-112">**\_режим перечисления \_ использование \_ \_ префа устройства**</span><span class="sxs-lookup"><span data-stu-id="c32ed-112">**ENUM\_MODE\_USE\_DEVICE\_PREF**</span></span>

<span data-ttu-id="c32ed-113">Перечисляет содержимое хранилища на основе настроек устройства, как указано в параметре устройства *усеметадатавиевс* .</span><span class="sxs-lookup"><span data-stu-id="c32ed-113">Enumerates content on the storage based on the device preference as indicated by the *UseMetadataViews* device parameter.</span></span>

<span data-ttu-id="c32ed-114">**\_ \_ представления метаданных в режиме перечисления \_**</span><span class="sxs-lookup"><span data-stu-id="c32ed-114">**ENUM\_MODE\_METADATA\_VIEWS**</span></span>

<span data-ttu-id="c32ed-115">Перечисляет содержимое в хранилище, организуя содержимое на основе представления метаданных.</span><span class="sxs-lookup"><span data-stu-id="c32ed-115">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> <dt>

<span data-ttu-id="c32ed-116"><span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**\_режим перечисления \_ использование \_ \_ префа устройства**</span><span class="sxs-lookup"><span data-stu-id="c32ed-116"><span id="ENUM_MODE_USE_DEVICE_PREF"></span><span id="enum_mode_use_device_pref"></span>**ENUM\_MODE\_USE\_DEVICE\_PREF**</span></span>
</dt> <dd>

<span data-ttu-id="c32ed-117">Перечисляет содержимое хранилища на основе настроек устройства, как указано в параметре устройства *усеметадатавиевс* .</span><span class="sxs-lookup"><span data-stu-id="c32ed-117">Enumerates content on the storage based on the device preference as indicated by the *UseMetadataViews* device parameter.</span></span>

<span data-ttu-id="c32ed-118">**\_ \_ представления метаданных в режиме перечисления \_**</span><span class="sxs-lookup"><span data-stu-id="c32ed-118">**ENUM\_MODE\_METADATA\_VIEWS**</span></span>

<span data-ttu-id="c32ed-119">Перечисляет содержимое в хранилище, организуя содержимое на основе представления метаданных.</span><span class="sxs-lookup"><span data-stu-id="c32ed-119">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> <dt>

<span data-ttu-id="c32ed-120"><span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**\_ \_ представления метаданных в режиме перечисления \_**</span><span class="sxs-lookup"><span data-stu-id="c32ed-120"><span id="ENUM_MODE_METADATA_VIEWS"></span><span id="enum_mode_metadata_views"></span>**ENUM\_MODE\_METADATA\_VIEWS**</span></span>
</dt> <dd>

<span data-ttu-id="c32ed-121">Перечисляет содержимое в хранилище, организуя содержимое на основе представления метаданных.</span><span class="sxs-lookup"><span data-stu-id="c32ed-121">Enumerates content on the storage by organizing the content based on a metadata view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c32ed-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c32ed-122">Requirements</span></span>



| <span data-ttu-id="c32ed-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c32ed-123">Requirement</span></span> | <span data-ttu-id="c32ed-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c32ed-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c32ed-125">Header</span><span class="sxs-lookup"><span data-stu-id="c32ed-125">Header</span></span><br/> | <dl> <span data-ttu-id="c32ed-126"><dt>Вмдм. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c32ed-126"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c32ed-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c32ed-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c32ed-128">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="c32ed-128">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





