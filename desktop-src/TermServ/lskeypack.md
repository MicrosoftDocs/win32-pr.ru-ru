---
title: Структура Лскэйпакк
description: Содержит сведения о конкретном пакете лицензионных ключей службы удаленных рабочих столов.
ms.assetid: c26d27ee-7dd3-49f0-a79c-752d23693a2a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов структуры Лскэйпакк
- службы удаленных рабочих столов указателя структуры Лплскэйпакк
topic_type:
- apiref
api_name:
- LSKeyPack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b1ac1f51e66a0a3c15c33f2535bc02f1fd3528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989246"
---
# <a name="lskeypack-structure"></a><span data-ttu-id="c9675-105">Структура Лскэйпакк</span><span class="sxs-lookup"><span data-stu-id="c9675-105">LSKeyPack structure</span></span>

<span data-ttu-id="c9675-106">Содержит сведения о конкретном пакете лицензионных ключей службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c9675-106">Contains information about a specific Remote Desktop Services licensing key pack.</span></span>

> [!Note]  
> <span data-ttu-id="c9675-107">Эта структура не определена ни в одном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="c9675-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="c9675-108">Чтобы использовать эту структуру, необходимо определить ее самостоятельно, как показано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="c9675-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c9675-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9675-109">Syntax</span></span>


```C++
typedef struct _LSKeyPack {
  DWORD dwVersion;
  UCHAR ucKeyPackType;
  TCHAR szCompanyName[256];
  TCHAR szKeyPackId[256];
  TCHAR szProductName[256];
  TCHAR szProductId[256];
  TCHAR szProductDesc[256];
  WORD  wMajorVersion;
  WORD  wMinorVersion;
  DWORD dwPlatformType;
  UCHAR ucLicenseType;
  DWORD dwLanguageId;
  UCHAR ucChannelOfPurchase;
  TCHAR szBeginSerialNumber[256];
  DWORD dwTotalLicenseInKeyPack;
  DWORD dwProductFlags;
  DWORD dwKeyPackId;
  UCHAR ucKeyPackStatus;
  DWORD dwActivateDate;
  DWORD dwExpirationDate;
  DWORD dwNumberOfLicenses;
} LSKeyPack, *LPLSKeyPack;
```



## <a name="members"></a><span data-ttu-id="c9675-110">Члены</span><span class="sxs-lookup"><span data-stu-id="c9675-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="c9675-111">**двверсион**</span><span class="sxs-lookup"><span data-stu-id="c9675-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-112">Версия пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="c9675-112">Version of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-113">**уккэйпакктипе**</span><span class="sxs-lookup"><span data-stu-id="c9675-113">**ucKeyPackType**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-114">Тип пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="c9675-114">Type of key pack.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-115">**сзкомпанинаме**</span><span class="sxs-lookup"><span data-stu-id="c9675-115">**szCompanyName**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-116">Название компании, выдавшей пакет ключей.</span><span class="sxs-lookup"><span data-stu-id="c9675-116">Name of the company that issued the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-117">**сзкэйпаккид**</span><span class="sxs-lookup"><span data-stu-id="c9675-117">**szKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-118">Идентификатор пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="c9675-118">ID of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-119">**сзпродуктнаме**</span><span class="sxs-lookup"><span data-stu-id="c9675-119">**szProductName**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-120">Имя продукта, которому принадлежит этот пакет ключей.</span><span class="sxs-lookup"><span data-stu-id="c9675-120">Name of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-121">**сзпродуктид**</span><span class="sxs-lookup"><span data-stu-id="c9675-121">**szProductId**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-122">Идентификатор продукта, которому принадлежит этот пакет ключей.</span><span class="sxs-lookup"><span data-stu-id="c9675-122">ID of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-123">**сзпродуктдеск**</span><span class="sxs-lookup"><span data-stu-id="c9675-123">**szProductDesc**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-124">Описание продукта, которому принадлежит этот пакет ключей.</span><span class="sxs-lookup"><span data-stu-id="c9675-124">Description of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-125">**вмажорверсион**</span><span class="sxs-lookup"><span data-stu-id="c9675-125">**wMajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-126">Основной номер версии продукта, к которому относится этот пакет ключей.</span><span class="sxs-lookup"><span data-stu-id="c9675-126">Major version of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-127">**вминорверсион**</span><span class="sxs-lookup"><span data-stu-id="c9675-127">**wMinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-128">Дополнительный номер версии продукта, к которому относится этот пакет ключей.</span><span class="sxs-lookup"><span data-stu-id="c9675-128">Minor version of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-129">**двплатформтипе**</span><span class="sxs-lookup"><span data-stu-id="c9675-129">**dwPlatformType**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-130">Тип платформы.</span><span class="sxs-lookup"><span data-stu-id="c9675-130">Platform type.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-131">**уклиценсетипе**</span><span class="sxs-lookup"><span data-stu-id="c9675-131">**ucLicenseType**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-132">Тип лицензий в пакете ключей.</span><span class="sxs-lookup"><span data-stu-id="c9675-132">Type of licenses in the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-133">**двлангуажеид**</span><span class="sxs-lookup"><span data-stu-id="c9675-133">**dwLanguageId**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-134">Идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="c9675-134">Language ID.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-135">**укчаннелофпурчасе**</span><span class="sxs-lookup"><span data-stu-id="c9675-135">**ucChannelOfPurchase**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-136">Канал покупки.</span><span class="sxs-lookup"><span data-stu-id="c9675-136">Channel of purchase.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-137">**сзбегинсериалнумбер**</span><span class="sxs-lookup"><span data-stu-id="c9675-137">**szBeginSerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-138">Серийный номер первой лицензии.</span><span class="sxs-lookup"><span data-stu-id="c9675-138">Serial number for the first license.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-139">**двтоталлиценсеинкэйпакк**</span><span class="sxs-lookup"><span data-stu-id="c9675-139">**dwTotalLicenseInKeyPack**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-140">Общее число лицензий в пакете ключей.</span><span class="sxs-lookup"><span data-stu-id="c9675-140">Total number of licenses in the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-141">**двпродуктфлагс**</span><span class="sxs-lookup"><span data-stu-id="c9675-141">**dwProductFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-142">Метки.</span><span class="sxs-lookup"><span data-stu-id="c9675-142">Flags.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-143">**двкэйпаккид**</span><span class="sxs-lookup"><span data-stu-id="c9675-143">**dwKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-144">Идентификатор пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="c9675-144">ID of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-145">**уккэйпаккстатус**</span><span class="sxs-lookup"><span data-stu-id="c9675-145">**ucKeyPackStatus**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-146">Состояние пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="c9675-146">Status of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-147">**двактиватедате**</span><span class="sxs-lookup"><span data-stu-id="c9675-147">**dwActivateDate**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-148">Дата активации пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="c9675-148">Activation date for the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-149">**двекспиратиондате**</span><span class="sxs-lookup"><span data-stu-id="c9675-149">**dwExpirationDate**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-150">Дата истечения срока действия пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="c9675-150">Expiration date for the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="c9675-151">**двнумберофлиценсес**</span><span class="sxs-lookup"><span data-stu-id="c9675-151">**dwNumberOfLicenses**</span></span>
</dt> <dd>

<span data-ttu-id="c9675-152">Число лицензий.</span><span class="sxs-lookup"><span data-stu-id="c9675-152">Number of licenses.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9675-153">Требования</span><span class="sxs-lookup"><span data-stu-id="c9675-153">Requirements</span></span>



| <span data-ttu-id="c9675-154">Требование</span><span class="sxs-lookup"><span data-stu-id="c9675-154">Requirement</span></span> | <span data-ttu-id="c9675-155">Значение</span><span class="sxs-lookup"><span data-stu-id="c9675-155">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c9675-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9675-156">Minimum supported client</span></span><br/> | <span data-ttu-id="c9675-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9675-157">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c9675-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9675-158">Minimum supported server</span></span><br/> | <span data-ttu-id="c9675-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9675-159">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9675-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9675-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9675-161">**тлскэйпаккенумбегин**</span><span class="sxs-lookup"><span data-stu-id="c9675-161">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dt>

[<span data-ttu-id="c9675-162">**тлскэйпаккенумнекст**</span><span class="sxs-lookup"><span data-stu-id="c9675-162">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dt>

[<span data-ttu-id="c9675-163">**тлскэйпаккенуменд**</span><span class="sxs-lookup"><span data-stu-id="c9675-163">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

 





