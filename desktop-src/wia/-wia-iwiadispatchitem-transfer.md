---
description: Метод Transfer объекта Item передает данные с устройства в файл. Этот метод применяется только к элементам типа устройства.
ms.assetid: ed9696da-bd94-4063-80c2-311a7a441b10
title: Item. Перемещение, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.Transfer
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: a476f9653b7deced48394af0ecaa0ea0c8ae51e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692523"
---
# <a name="itemtransfer-method"></a><span data-ttu-id="c1cc2-104">Item. Перемещение, метод</span><span class="sxs-lookup"><span data-stu-id="c1cc2-104">Item.Transfer method</span></span>

<span data-ttu-id="c1cc2-105">Метод **Transfer** объекта [**Item**](-wia-item.md) передает данные с устройства в файл.</span><span class="sxs-lookup"><span data-stu-id="c1cc2-105">The **Transfer** method of the [**Item**](-wia-item.md) object transfers data from a device to a file.</span></span> <span data-ttu-id="c1cc2-106">Этот метод применяется только к элементам типа устройства.</span><span class="sxs-lookup"><span data-stu-id="c1cc2-106">This method applies only to device type items.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1cc2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1cc2-107">Syntax</span></span>


```JScript
Item.Transfer(
  Filename,
  AsyncTransfer = VARIANT_BOOL
)
```



## <a name="parameters"></a><span data-ttu-id="c1cc2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1cc2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1cc2-109">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1cc2-109">*Filename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cc2-110">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c1cc2-110">Type: **BSTR**</span></span>

<span data-ttu-id="c1cc2-111">Указывает имя файла, в который передаются данные.</span><span class="sxs-lookup"><span data-stu-id="c1cc2-111">Specifies the name of the file to which the data is transferred.</span></span>

</dd> <dt>

<span data-ttu-id="c1cc2-112">*Асинктрансфер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1cc2-112">*AsyncTransfer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cc2-113">Тип: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="c1cc2-113">Type: **VARIANT\_BOOL**</span></span>

<span data-ttu-id="c1cc2-114">Логическое значение, указывающее, следует ли выполнять пересылку как асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="c1cc2-114">A Boolean value that specifies whether the transfer should be run as an asynchronous call.</span></span>

<dt>



 <span data-ttu-id="c1cc2-115">(Вариант \_ ЛОГИЧЕСКОМ</span><span class="sxs-lookup"><span data-stu-id="c1cc2-115">(VARIANT\_BOOL)</span></span>


</dt> <dd>

<span data-ttu-id="c1cc2-116">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c1cc2-116">Default.</span></span> <span data-ttu-id="c1cc2-117">Задайте для этого параметра значение **true** , если вызов должен быть асинхронным (см. **Примечания**).</span><span class="sxs-lookup"><span data-stu-id="c1cc2-117">Set this value to **true** if the call should be asynchronous (see **Remarks**).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1cc2-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1cc2-118">Return value</span></span>

<span data-ttu-id="c1cc2-119">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c1cc2-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1cc2-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1cc2-120">Remarks</span></span>

<span data-ttu-id="c1cc2-121">Этот метод применяется только к элементам типа файлов.</span><span class="sxs-lookup"><span data-stu-id="c1cc2-121">This method applies only to file type items.</span></span> <span data-ttu-id="c1cc2-122">Метод проверяет, что элемент поддерживает этот метод, прежде чем он попытается выполнить пересылку данных.</span><span class="sxs-lookup"><span data-stu-id="c1cc2-122">The method checks that the item supports this method before it attempts to complete the data transfer.</span></span>

<span data-ttu-id="c1cc2-123">Используйте "Clipboard" в качестве параметра *filename* для перемещения элемента в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="c1cc2-123">Use "clipboard" as the *Filename* parameter to transfer an item to the clipboard.</span></span>

<span data-ttu-id="c1cc2-124">Задайте для параметра *асинктрансфер* значение **false** для передачи в любом приложении или сценарии, работающем в среде, завершающей процесс в конце скрипта, например сервер сценариев Windows (WSH).</span><span class="sxs-lookup"><span data-stu-id="c1cc2-124">Set the *AsyncTransfer* value to **false** for transfers within any application or script that runs in an environment that terminates a process at the end of a script, such as Windows Script Host (WSH).</span></span> <span data-ttu-id="c1cc2-125">В противном случае скрипт может завершиться, а процесс завершится до завершения перемещения.</span><span class="sxs-lookup"><span data-stu-id="c1cc2-125">Otherwise, the script may end, and the process terminate, before the transfer completes.</span></span>

<span data-ttu-id="c1cc2-126">Метод **передачи** не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="c1cc2-126">The **Transfer** method has no return value.</span></span> <span data-ttu-id="c1cc2-127">После завершения перемещения этот метод отправляет событие [**онтрансферкомплете**](-wia--iwiaevents-ontransfercomplete.md) в скрипт или приложение.</span><span class="sxs-lookup"><span data-stu-id="c1cc2-127">Upon completion of a transfer, this method sends an [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md) event to the script or application.</span></span>

## <a name="examples"></a><span data-ttu-id="c1cc2-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="c1cc2-128">Examples</span></span>

<span data-ttu-id="c1cc2-129">В следующем примере демонстрируется использование метода **перемещения** для перемещения данных с устройства.</span><span class="sxs-lookup"><span data-stu-id="c1cc2-129">The following example demonstrates the use of the **Transfer** method to transfer data from a device.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItems
        objItem.Transfer("c:\Folder\Filename.bmp")
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="c1cc2-130">Требования</span><span class="sxs-lookup"><span data-stu-id="c1cc2-130">Requirements</span></span>



| <span data-ttu-id="c1cc2-131">Требование</span><span class="sxs-lookup"><span data-stu-id="c1cc2-131">Requirement</span></span> | <span data-ttu-id="c1cc2-132">Значение</span><span class="sxs-lookup"><span data-stu-id="c1cc2-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1cc2-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1cc2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c1cc2-134">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c1cc2-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c1cc2-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1cc2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c1cc2-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c1cc2-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c1cc2-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c1cc2-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1cc2-138"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="c1cc2-138"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




