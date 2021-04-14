---
description: 'Для Windows 7 портативные устройства Windows поддерживают следующие атрибуты для форматов в службе устройств. Эти атрибуты возвращаются методом Ипортабледевицесервицекапабилитиес:: Жетформататтрибутес.'
ms.assetid: 53282e01-54da-4adf-8a09-2086d6398275
title: Атрибуты формата (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Format
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 559f731ec7d61007b05e4625ff67488b5ef482fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668680"
---
# <a name="format-attributes"></a><span data-ttu-id="96744-104">Атрибуты формата</span><span class="sxs-lookup"><span data-stu-id="96744-104">Format Attributes</span></span>

<span data-ttu-id="96744-105">Для Windows 7 портативные устройства Windows поддерживают следующие атрибуты для форматов в службе устройств.</span><span class="sxs-lookup"><span data-stu-id="96744-105">For Windows 7, Windows Portable Devices supports the following attributes for formats on a device service.</span></span> <span data-ttu-id="96744-106">Эти атрибуты возвращаются методом [**ипортабледевицесервицекапабилитиес:: жетформататтрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) .</span><span class="sxs-lookup"><span data-stu-id="96744-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method.</span></span>




| <span data-ttu-id="96744-107">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="96744-107">**Attribute**</span></span>                        | <span data-ttu-id="96744-108">**VarType**</span><span class="sxs-lookup"><span data-stu-id="96744-108">**VarType**</span></span>    | <span data-ttu-id="96744-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="96744-109">**Description**</span></span>                                                                                                           |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96744-110">**\_ \_ тип MIME атрибута формата WPD \_**</span><span class="sxs-lookup"><span data-stu-id="96744-110">**WPD\_FORMAT\_ATTRIBUTE\_MIMETYPE**</span></span> | <span data-ttu-id="96744-111">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="96744-111">**VT\_LPWSTR**</span></span> | <span data-ttu-id="96744-112">Тип MIME формата.</span><span class="sxs-lookup"><span data-stu-id="96744-112">The format MIME type.</span></span>                                                                                                     |
| <span data-ttu-id="96744-113">**\_ \_ имя атрибута формата \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="96744-113">**WPD\_FORMAT\_ATTRIBUTE\_NAME**</span></span>     | <span data-ttu-id="96744-114">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="96744-114">**VT\_LPWSTR**</span></span> | <span data-ttu-id="96744-115">Строка, указывающая понятное для сценария имя формата.</span><span class="sxs-lookup"><span data-stu-id="96744-115">A string that specifies the script-friendly name of the format.</span></span> <span data-ttu-id="96744-116">Допустимые символы: алфавитные буквы \[ a-zA-Z0-9 \] и " \_ ".</span><span class="sxs-lookup"><span data-stu-id="96744-116">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="96744-117">Требования</span><span class="sxs-lookup"><span data-stu-id="96744-117">Requirements</span></span>



| <span data-ttu-id="96744-118">Требование</span><span class="sxs-lookup"><span data-stu-id="96744-118">Requirement</span></span> | <span data-ttu-id="96744-119">Значение</span><span class="sxs-lookup"><span data-stu-id="96744-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="96744-120">Header</span><span class="sxs-lookup"><span data-stu-id="96744-120">Header</span></span><br/> | <dl> <span data-ttu-id="96744-121"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="96744-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96744-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96744-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96744-123">**Свойства и атрибуты**</span><span class="sxs-lookup"><span data-stu-id="96744-123">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




