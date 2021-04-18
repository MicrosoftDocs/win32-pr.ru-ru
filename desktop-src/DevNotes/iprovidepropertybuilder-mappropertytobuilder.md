---
description: Проверяет, связан ли конструктор с определенным свойством.
ms.assetid: 8fab2dc2-3549-4559-b704-6783d929274e
title: 'Метод Ипровидепропертибуилдер:: Маппропертитобуилдер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.MapPropertyToBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: 5fa755449bfb97940235fe45f9e299aa828e6faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665262"
---
# <a name="iprovidepropertybuildermappropertytobuilder-method"></a><span data-ttu-id="693f4-103">Метод Ипровидепропертибуилдер:: Маппропертитобуилдер</span><span class="sxs-lookup"><span data-stu-id="693f4-103">IProvidePropertyBuilder::MapPropertyToBuilder method</span></span>

<span data-ttu-id="693f4-104">Проверяет, связан ли конструктор с определенным свойством.</span><span class="sxs-lookup"><span data-stu-id="693f4-104">Checks whether a builder should be associated with a particular property.</span></span>

## <a name="syntax"></a><span data-ttu-id="693f4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="693f4-105">Syntax</span></span>


```C++
void MapPropertyToBuilder(
  [in]          LONG   dispid,
  [out]         DWORD  *pdwCtlBldType,
  [out]         LPBSTR pbstrGuidBldr,
  [out, retval] LPBOOL builderAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="693f4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="693f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="693f4-107">*идентификатор DISPID* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="693f4-107">*dispid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="693f4-108">Идентификатор DISPID рассматриваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="693f4-108">The DISPID of the property in question.</span></span>

</dd> <dt>

<span data-ttu-id="693f4-109">*пдвктлблдтипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="693f4-109">*pdwCtlBldType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="693f4-110">Построитель для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="693f4-110">The builder to be mapped.</span></span> <span data-ttu-id="693f4-111">Этот параметр может быть сочетанием следующих значений.</span><span class="sxs-lookup"><span data-stu-id="693f4-111">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="693f4-112">Значение</span><span class="sxs-lookup"><span data-stu-id="693f4-112">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="693f4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="693f4-113">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="CTLBLDTYPE_FSTDPROPBUILDER"></span><span id="ctlbldtype_fstdpropbuilder"></span><dl> <span data-ttu-id="693f4-114"><dt>**Ктлблдтипе \_ ФСТДПРОПБУИЛДЕР**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="693f4-114"><dt>**CTLBLDTYPE\_FSTDPROPBUILDER**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="693f4-115">Вызов стандартного системного конструктора (не поддерживается в Visual Studio).</span><span class="sxs-lookup"><span data-stu-id="693f4-115">Invoke a standard system builder (not supported in Visual Studio).</span></span><br/> |
| <span id="CTLBLDTYPE_FINTERNALBUILDER"></span><span id="ctlbldtype_finternalbuilder"></span><dl> <span data-ttu-id="693f4-116"><dt>**Ктлблдтипе \_ ФИНТЕРНАЛБУИЛДЕР**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="693f4-116"><dt>**CTLBLDTYPE\_FINTERNALBUILDER**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="693f4-117">Вызовите пользовательский сборщик.</span><span class="sxs-lookup"><span data-stu-id="693f4-117">Invoke a custom builder.</span></span><br/>                                           |
| <span id="CTLBLDTYPE_EDITSOBJDIRECTLY"></span><span id="ctlbldtype_editsobjdirectly"></span><dl> <span data-ttu-id="693f4-118"><dt>**Ктлблдтипе \_ ЕДИТСОБЖДИРЕКТЛИ**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="693f4-118"><dt>**CTLBLDTYPE\_EDITSOBJDIRECTLY**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="693f4-119">Построитель изменяет объект.</span><span class="sxs-lookup"><span data-stu-id="693f4-119">Builder modifies the object.</span></span> <span data-ttu-id="693f4-120">Это обычное поведение.</span><span class="sxs-lookup"><span data-stu-id="693f4-120">This is common behavior.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="693f4-121">*пбстргуидблдр* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="693f4-121">*pbstrGuidBldr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="693f4-122">Идентификатор GUID, определяющий построитель для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="693f4-122">The GUID that identifies the builder for this property.</span></span>

</dd> <dt>

<span data-ttu-id="693f4-123">*буилдераваилабле* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="693f4-123">*builderAvailable* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="693f4-124">Этот параметр имеет **значение true** , если это свойство в настоящее время поддерживает построитель.</span><span class="sxs-lookup"><span data-stu-id="693f4-124">This parameter is **TRUE** if this property currently supports a builder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="693f4-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="693f4-125">Return value</span></span>

<span data-ttu-id="693f4-126">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="693f4-126">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="693f4-127">Требования</span><span class="sxs-lookup"><span data-stu-id="693f4-127">Requirements</span></span>



| <span data-ttu-id="693f4-128">Требование</span><span class="sxs-lookup"><span data-stu-id="693f4-128">Requirement</span></span> | <span data-ttu-id="693f4-129">Значение</span><span class="sxs-lookup"><span data-stu-id="693f4-129">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="693f4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="693f4-130">DLL</span></span><br/> | <dl> <span data-ttu-id="693f4-131"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="693f4-131"><dt>Vsp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="693f4-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="693f4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="693f4-133">**ипровидепропертибуилдер**</span><span class="sxs-lookup"><span data-stu-id="693f4-133">**IProvidePropertyBuilder**</span></span>](iprovidepropertybuilder.md)
</dt> </dl>

 

 




