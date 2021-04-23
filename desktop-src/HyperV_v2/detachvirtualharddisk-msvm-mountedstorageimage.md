---
description: Отсоединяет образ подключенного хранилища, связанный с этим классом.
ms.assetid: C3AB0EEE-71FE-4049-90AB-01F5D77E3B97
title: Метод Детачвиртуалхарддиск класса Msvm_MountedStorageImage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MountedStorageImage.DetachVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0d411134d85fe70163b2e08eebed0ff0d4b88e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683975"
---
# <a name="detachvirtualharddisk-method-of-the-msvm_mountedstorageimage-class"></a><span data-ttu-id="1ba28-103">Метод Детачвиртуалхарддиск \_ класса Маунтедсторажеимаже мсвм</span><span class="sxs-lookup"><span data-stu-id="1ba28-103">DetachVirtualHardDisk method of the Msvm\_MountedStorageImage class</span></span>

<span data-ttu-id="1ba28-104">Отсоединяет образ подключенного хранилища, связанный с этим классом.</span><span class="sxs-lookup"><span data-stu-id="1ba28-104">Detaches the mounted storage image that is associated with this class.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ba28-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ba28-105">Syntax</span></span>


```mof
uint32 DetachVirtualHardDisk();
```



## <a name="parameters"></a><span data-ttu-id="1ba28-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ba28-106">Parameters</span></span>

<span data-ttu-id="1ba28-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1ba28-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1ba28-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ba28-108">Return value</span></span>

<span data-ttu-id="1ba28-109">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ba28-109">Type: **uint32**</span></span>

<span data-ttu-id="1ba28-110">Этот метод может возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1ba28-110">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1ba28-111">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="1ba28-111">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ba28-112">**Сбой** (1)</span><span class="sxs-lookup"><span data-stu-id="1ba28-112">**Failed** (1)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="1ba28-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ba28-113">Remarks</span></span>

<span data-ttu-id="1ba28-114">Доступ к классу [**\_ маунтедсторажеимаже мсвм**](msvm-mountedstorageimage.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="1ba28-114">Access to the [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1ba28-115">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1ba28-115">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="1ba28-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="1ba28-116">Examples</span></span>

<span data-ttu-id="1ba28-117">В следующем примере C# показано, как отсоединить файл виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="1ba28-117">The following C# example shows how to detach a virtual hard disk file.</span></span> <span data-ttu-id="1ba28-118">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="1ba28-118">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void DetachVirtualHardDisk(string path)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);

    ManagementClass mountedStorageImageServiceClass = new ManagementClass("Msvm_MountedStorageImage");

    mountedStorageImageServiceClass.Scope = scope;

    using (ManagementObjectCollection collection = mountedStorageImageServiceClass.GetInstances())
    {
        foreach (ManagementObject image in collection)
        {
            using (image)
            {
                string name = image.GetPropertyValue("Name").ToString();
                if (string.Equals(name, path, StringComparison.OrdinalIgnoreCase))
                {
                    ManagementBaseObject outParams = image.InvokeMethod("DetachVirtualHardDisk", null, null);

                    if ((UInt32)outParams["ReturnValue"] == 0)
                    {
                        Console.WriteLine("{0} was detached successfully.", path);
                    }
                    else
                    {
                        Console.WriteLine("Unable to dettach {0}", path);
                    }

                    outParams.Dispose();

                    break;
                }

                image.Dispose();
            }
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="1ba28-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1ba28-119">Requirements</span></span>



| <span data-ttu-id="1ba28-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1ba28-120">Requirement</span></span> | <span data-ttu-id="1ba28-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1ba28-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ba28-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ba28-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1ba28-123">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1ba28-123">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1ba28-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ba28-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1ba28-125">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1ba28-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ba28-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1ba28-126">Namespace</span></span><br/>                | <span data-ttu-id="1ba28-127">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="1ba28-127">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1ba28-128">MOF</span><span class="sxs-lookup"><span data-stu-id="1ba28-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ba28-129"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ba28-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ba28-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1ba28-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ba28-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1ba28-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1ba28-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ba28-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ba28-133">**Мсвм \_ маунтедсторажеимаже**</span><span class="sxs-lookup"><span data-stu-id="1ba28-133">**Msvm\_MountedStorageImage**</span></span>](msvm-mountedstorageimage.md)
</dt> </dl>

 

