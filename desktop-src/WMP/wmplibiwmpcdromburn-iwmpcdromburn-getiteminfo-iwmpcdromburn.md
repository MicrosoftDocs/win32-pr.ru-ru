---
title: Ивмпкдромбурн getItemInfo, метод
description: Метод getItemInfo извлекает значение указанного атрибута для компакт-диска.
ms.assetid: 9ca54ec4-42be-40c1-931e-c3bfcbc2b370
keywords:
- getItemInfo метод Windows Media Player
- getItemInfo метод проигрывателя Windows Media Player, интерфейс Ивмпкдромбурн
- Интерфейс Ивмпкдромбурн Windows Media Player, метод getItemInfo
topic_type:
- apiref
api_name:
- IWMPCdromBurn.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9030bd230b2e17bab6ad54dc762a78d2cb343d03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717981"
---
# <a name="iwmpcdromburngetiteminfo-method"></a><span data-ttu-id="7fdb2-106">Метод Ивмпкдромбурн:: getItemInfo</span><span class="sxs-lookup"><span data-stu-id="7fdb2-106">IWMPCdromBurn::getItemInfo method</span></span>

<span data-ttu-id="7fdb2-107">Метод **getItemInfo** извлекает значение указанного атрибута для компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="7fdb2-107">The **getItemInfo** method retrieves the value of the specified attribute for the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fdb2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7fdb2-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrItem
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItem As System.String _
) As System.String
Implements IWMPCdromBurn.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="7fdb2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7fdb2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fdb2-110">*бстритем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7fdb2-110">*bstrItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fdb2-111">**Строка System. String** , которая содержит одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7fdb2-111">A **System.String** that contains one of the following values.</span></span>



| <span data-ttu-id="7fdb2-112">Значение</span><span class="sxs-lookup"><span data-stu-id="7fdb2-112">Value</span></span>         | <span data-ttu-id="7fdb2-113">Описание</span><span class="sxs-lookup"><span data-stu-id="7fdb2-113">Description</span></span>                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fdb2-114">аваилаблетиме</span><span class="sxs-lookup"><span data-stu-id="7fdb2-114">AvailableTime</span></span> | <span data-ttu-id="7fdb2-115">Получение времени, доступного на компакт-диске в секундах.</span><span class="sxs-lookup"><span data-stu-id="7fdb2-115">Retrieves the time available on the CD, in seconds.</span></span>                                          |
| <span data-ttu-id="7fdb2-116">Пусто</span><span class="sxs-lookup"><span data-stu-id="7fdb2-116">Blank</span></span>         | <span data-ttu-id="7fdb2-117">Извлекает значение **System. Boolean** (представленное в виде строки), указывающее, является ли компакт-диск пустым.</span><span class="sxs-lookup"><span data-stu-id="7fdb2-117">Retrieves a **System.Boolean** (represented as a string) indicating whether the CD is blank.</span></span> |
| <span data-ttu-id="7fdb2-118">FreeSpace</span><span class="sxs-lookup"><span data-stu-id="7fdb2-118">FreeSpace</span></span>     | <span data-ttu-id="7fdb2-119">Получение свободного места на компакт-диске в байтах.</span><span class="sxs-lookup"><span data-stu-id="7fdb2-119">Retrieves the free space on the CD, in bytes.</span></span>                                                |
| <span data-ttu-id="7fdb2-120">тоталспаце</span><span class="sxs-lookup"><span data-stu-id="7fdb2-120">TotalSpace</span></span>    | <span data-ttu-id="7fdb2-121">Возвращает общее пространство на компакт-диске в байтах.</span><span class="sxs-lookup"><span data-stu-id="7fdb2-121">Retrieves the total space on the CD, in bytes.</span></span>                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fdb2-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7fdb2-122">Return value</span></span>

<span data-ttu-id="7fdb2-123">**Строка System. String** , которая является значением указанного атрибута.</span><span class="sxs-lookup"><span data-stu-id="7fdb2-123">A **System.String** that is the value of the specified attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fdb2-124">Требования</span><span class="sxs-lookup"><span data-stu-id="7fdb2-124">Requirements</span></span>



| <span data-ttu-id="7fdb2-125">Требование</span><span class="sxs-lookup"><span data-stu-id="7fdb2-125">Requirement</span></span> | <span data-ttu-id="7fdb2-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7fdb2-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fdb2-127">Версия</span><span class="sxs-lookup"><span data-stu-id="7fdb2-127">Version</span></span><br/>   | <span data-ttu-id="7fdb2-128">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="7fdb2-128">Windows Media Player 11</span></span><br/>                                                                                     |
| <span data-ttu-id="7fdb2-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7fdb2-129">Namespace</span></span><br/> | <span data-ttu-id="7fdb2-130">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="7fdb2-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7fdb2-131">Сборка</span><span class="sxs-lookup"><span data-stu-id="7fdb2-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7fdb2-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7fdb2-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fdb2-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fdb2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fdb2-134">**Интерфейс Ивмпкдромбурн (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7fdb2-134">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





