---
description: Сохраняет шаблоны в файл DirectX. Не рекомендуется.
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: 'Метод Идиректксфилесавеобжект:: Саветемплатес (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3c63ae2e0f211aa8e7064161d03a66cafe1e8289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354670"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a><span data-ttu-id="18865-104">Метод Идиректксфилесавеобжект:: Саветемплатес</span><span class="sxs-lookup"><span data-stu-id="18865-104">IDirectXFileSaveObject::SaveTemplates method</span></span>

<span data-ttu-id="18865-105">Сохраняет шаблоны в файл DirectX.</span><span class="sxs-lookup"><span data-stu-id="18865-105">Saves templates to a DirectX file.</span></span> <span data-ttu-id="18865-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="18865-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="18865-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18865-107">Syntax</span></span>


```C++
HRESULT SaveTemplates(
  [in]       DWORD cTemplates,
  [in] const GUID  **ppguidTemplates
);
```



## <a name="parameters"></a><span data-ttu-id="18865-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="18865-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18865-109">*ктемплатес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18865-109">*cTemplates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18865-110">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18865-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18865-111">Общее число шаблонов для сохранения.</span><span class="sxs-lookup"><span data-stu-id="18865-111">Total number of templates to save.</span></span>

</dd> <dt>

<span data-ttu-id="18865-112">*ппгуидтемплатес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18865-112">*ppguidTemplates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18865-113">Тип: **константа [**GUID**](guid.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="18865-113">Type: **const [**GUID**](guid.md)\*\***</span></span>

<span data-ttu-id="18865-114">Адрес указателя на массив идентификаторов GUID для всех шаблонов, которые необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="18865-114">Address of a pointer to an array of the GUIDs for all templates to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18865-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18865-115">Return value</span></span>

<span data-ttu-id="18865-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="18865-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="18865-117">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="18865-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="18865-118">В случае сбоя метода возвращаемое значение может быть ДКСФИЛИРР \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="18865-118">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="18865-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18865-119">Remarks</span></span>

<span data-ttu-id="18865-120">В следующем фрагменте кода приведен пример вызова **идиректксфилесавеобжект:: саветемплатес** и примера содержимого для массива, в который указывает ппгуидтемплатес.</span><span class="sxs-lookup"><span data-stu-id="18865-120">The following code fragment provides an example call to **IDirectXFileSaveObject::SaveTemplates** and example contents for the array to which ppguidTemplates points.</span></span>


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



<span data-ttu-id="18865-121">После использования этого метода для сохранения шаблонов используйте метод [**идиректксфилесавеобжект:: креатедатаобжект**](idirectxfilesaveobject--createdataobject.md) , чтобы создать объект данных.</span><span class="sxs-lookup"><span data-stu-id="18865-121">After using this method to save the templates, use the [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) method to create a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="18865-122">Требования</span><span class="sxs-lookup"><span data-stu-id="18865-122">Requirements</span></span>



| <span data-ttu-id="18865-123">Требование</span><span class="sxs-lookup"><span data-stu-id="18865-123">Requirement</span></span> | <span data-ttu-id="18865-124">Значение</span><span class="sxs-lookup"><span data-stu-id="18865-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18865-125">Header</span><span class="sxs-lookup"><span data-stu-id="18865-125">Header</span></span><br/>  | <dl> <span data-ttu-id="18865-126"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="18865-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="18865-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="18865-127">Library</span></span><br/> | <dl> <span data-ttu-id="18865-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18865-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18865-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18865-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18865-130">идиректксфилесавеобжект</span><span class="sxs-lookup"><span data-stu-id="18865-130">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> <dt>

[<span data-ttu-id="18865-131">**Идиректксфилесавеобжект:: Креатедатаобжект**</span><span class="sxs-lookup"><span data-stu-id="18865-131">**IDirectXFileSaveObject::CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 
