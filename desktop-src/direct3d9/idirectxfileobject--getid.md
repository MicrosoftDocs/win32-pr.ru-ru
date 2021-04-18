---
description: Получает указатель на идентификатор GUID, определяющий объект файла DirectX. Не рекомендуется.
ms.assetid: 74c7a1d9-85e4-43eb-bcd8-1f3ddd713e9f
title: 'Метод Идиректксфилеобжект:: GetId (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetId
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 336dbde487ecd1b3af7b32d3743f037c235952f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105684992"
---
# <a name="idirectxfileobjectgetid-method"></a><span data-ttu-id="7ce1b-104">Метод Идиректксфилеобжект:: GetId</span><span class="sxs-lookup"><span data-stu-id="7ce1b-104">IDirectXFileObject::GetId method</span></span>

<span data-ttu-id="7ce1b-105">Получает указатель на идентификатор GUID, определяющий объект файла DirectX.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-105">Retrieves a pointer to the GUID that identifies a DirectX file object.</span></span> <span data-ttu-id="7ce1b-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ce1b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ce1b-107">Syntax</span></span>


```C++
HRESULT GetId(
  [out, retval] 
            LPGUID pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="7ce1b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ce1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ce1b-109">*пгуид* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7ce1b-109">*pGuid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7ce1b-110">Тип: **лпгуид**</span><span class="sxs-lookup"><span data-stu-id="7ce1b-110">Type: **LPGUID**</span></span>

<span data-ttu-id="7ce1b-111">Указатель на идентификатор GUID для получения идентификатора объекта.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-111">Pointer to a GUID to receive the object's ID.</span></span> <span data-ttu-id="7ce1b-112">Функция присвойте идентификатору GUID **значение NULL** , если у объекта нет идентификатора.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-112">The function will set the GUID to a **NULL** GUID if the object does not have an ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ce1b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ce1b-113">Return value</span></span>

<span data-ttu-id="7ce1b-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ce1b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ce1b-115">Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-115">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="7ce1b-116">В случае сбоя метода возвращаемое значение может быть ДКСФИЛИРР \_ бадвалуе.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-116">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ce1b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="7ce1b-117">Requirements</span></span>



| <span data-ttu-id="7ce1b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="7ce1b-118">Requirement</span></span> | <span data-ttu-id="7ce1b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="7ce1b-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7ce1b-120">Header</span><span class="sxs-lookup"><span data-stu-id="7ce1b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7ce1b-121"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ce1b-121"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ce1b-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7ce1b-122">Library</span></span><br/> | <dl> <span data-ttu-id="7ce1b-123"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ce1b-123"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ce1b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ce1b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ce1b-125">идиректксфилеобжект</span><span class="sxs-lookup"><span data-stu-id="7ce1b-125">IDirectXFileObject</span></span>](idirectxfileobject.md)
</dt> </dl>

 

 




