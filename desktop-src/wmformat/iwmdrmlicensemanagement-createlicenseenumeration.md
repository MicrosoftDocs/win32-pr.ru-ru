---
title: Метод Ивмдрмлиценсеманажемент Креателиценсинумератион (Вмдрмсдк. h)
description: Метод Креателиценсинумератион создает объект перечислителя лицензий, с помощью которого можно получить сведения о лицензиях в локальном хранилище лицензий.
ms.assetid: 48da1ef4-89bc-4cba-b5c9-0e202eb2986f
keywords:
- Формат Windows Media, Креателиценсинумератион метод
- Креателиценсинумератион метод Windows Media Format, интерфейс Ивмдрмлиценсеманажемент
- Интерфейс Ивмдрмлиценсеманажемент Windows Media Format, метод Креателиценсинумератион
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb75d21cc640da39c3679ac118ead629b24f719
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717791"
---
# <a name="iwmdrmlicensemanagementcreatelicenseenumeration-method"></a><span data-ttu-id="0865c-106">Метод Ивмдрмлиценсеманажемент:: Креателиценсинумератион</span><span class="sxs-lookup"><span data-stu-id="0865c-106">IWMDRMLicenseManagement::CreateLicenseEnumeration method</span></span>

<span data-ttu-id="0865c-107">Метод **креателиценсинумератион** создает объект перечислителя лицензий, с помощью которого можно получить сведения о лицензиях в локальном хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="0865c-107">The **CreateLicenseEnumeration** method creates a license enumerator object with which you can get information about licenses in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="0865c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0865c-108">Syntax</span></span>


```C++
HRESULT CreateLicenseEnumeration(
  [in]  WMDRM_LICENSE_FILTER *pLicenseFilter,
  [out] IWMDRMLicense        **pEnumerator
);
```



## <a name="parameters"></a><span data-ttu-id="0865c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0865c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0865c-110">*плиценсефилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0865c-110">*pLicenseFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0865c-111">Указатель на структуру [**\_ \_ фильтра лицензии WMDRM**](wmdrm-license-filter.md) , содержащую параметры фильтрации для списка лицензий в перечислителе.</span><span class="sxs-lookup"><span data-stu-id="0865c-111">Pointer to a [**WMDRM\_LICENSE\_FILTER**](wmdrm-license-filter.md) structure containing the filtering parameters for the list of licenses in the enumerator.</span></span>

</dd> <dt>

<span data-ttu-id="0865c-112">*пенумератор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0865c-112">*pEnumerator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0865c-113">Указатель, получающий адрес интерфейса [**ивмдрмлиценсе**](iwmdrmlicense.md) вновь созданного объекта перечислителя лицензии.</span><span class="sxs-lookup"><span data-stu-id="0865c-113">Pointer that receives the address of the [**IWMDRMLicense**](iwmdrmlicense.md) interface of the newly created license enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0865c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0865c-114">Return value</span></span>

<span data-ttu-id="0865c-115">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0865c-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0865c-116">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0865c-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0865c-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0865c-117">Return code</span></span>                                                                                                | <span data-ttu-id="0865c-118">Описание</span><span class="sxs-lookup"><span data-stu-id="0865c-118">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="0865c-119"><dt>**\_ \_ \_ \_ слишком \_ маленький Рив для NS E DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="0865c-119"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="0865c-120">Требуется обновленный список отзыва содержимого.</span><span class="sxs-lookup"><span data-stu-id="0865c-120">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="0865c-121"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0865c-121"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="0865c-122">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="0865c-122">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="0865c-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0865c-123">Remarks</span></span>

<span data-ttu-id="0865c-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="0865c-124">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="0865c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="0865c-125">Requirements</span></span>



| <span data-ttu-id="0865c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="0865c-126">Requirement</span></span> | <span data-ttu-id="0865c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="0865c-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0865c-128">Header</span><span class="sxs-lookup"><span data-stu-id="0865c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0865c-129"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="0865c-129"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="0865c-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0865c-130">Library</span></span><br/> | <dl> <span data-ttu-id="0865c-131"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0865c-131"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0865c-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0865c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0865c-133">**Перечисление лицензий в локальном хранилище лицензий**</span><span class="sxs-lookup"><span data-stu-id="0865c-133">**Enumerating Licenses in the Local License Store**</span></span>](enumerating-licenses-in-the-local-license-store.md)
</dt> <dt>

[<span data-ttu-id="0865c-134">**Интерфейс Ивмдрмлиценсеманажемент**</span><span class="sxs-lookup"><span data-stu-id="0865c-134">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





