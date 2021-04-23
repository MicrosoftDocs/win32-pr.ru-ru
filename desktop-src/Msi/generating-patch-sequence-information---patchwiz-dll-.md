---
description: Версия PATCHWIZ.DLL, выпущенная с установщик Windows&\# 160; 3.0, может автоматически создавать сведения о последовательности исправлений и добавлять в таблицу мсипатчсекуенце новое исправление.
ms.assetid: 03e7eea6-1a37-4c86-a9da-109fbaf20728
title: Создание сведений о последовательности исправлений (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff82166f33266a58cd3ef299b2546b04a94ebb14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998808"
---
# <a name="generating-patch-sequence-information-patchwizdll"></a><span data-ttu-id="97904-103">Создание сведений о последовательности исправлений (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="97904-103">Generating Patch Sequence Information (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="97904-104">Версия [PATCHWIZ.DLL](patchwiz-dll.md) , выпущенная с установщик Windows 3,0, может автоматически формировать сведения о последовательности обновлений и добавлять в [таблицу мсипатчсекуенце](msipatchsequence-table.md) новое исправление.</span><span class="sxs-lookup"><span data-stu-id="97904-104">The version of [PATCHWIZ.DLL](patchwiz-dll.md) released with Windows Installer 3.0 can automatically generate patch sequencing information and add to the [MsiPatchSequence Table](msipatchsequence-table.md) a new patch.</span></span>

<span data-ttu-id="97904-105">Задайте для свойства "Создание данных последовательностей" значение \_ \_ \_ 1 (одно) в [таблице свойств](properties-table-patchwiz-dll-.md) файла PCP, чтобы предотвратить автоматическое создание сведений о последовательности исправлений.</span><span class="sxs-lookup"><span data-stu-id="97904-105">Set the SEQUENCE\_DATA\_GENERATION\_DISABLED property to 1 (one) in the [Properties Table](properties-table-patchwiz-dll-.md) of the .pcp file to prevent the automatic generation of patch sequencing information.</span></span> <span data-ttu-id="97904-106">Если это свойство отсутствует, данные автоматически создаются и добавляются.</span><span class="sxs-lookup"><span data-stu-id="97904-106">If this property is absent, the information is automatically generated and added.</span></span>

<span data-ttu-id="97904-107">Если [PATCHWIZ.DLL](patchwiz-dll.md) , выпущенный с установщик Windows 3,0, используется для автоматического создания сведений о последовательности обновлений, происходит следующее.</span><span class="sxs-lookup"><span data-stu-id="97904-107">When the [PATCHWIZ.DLL](patchwiz-dll.md) released with Windows Installer 3.0 is used to automatically generate the patch sequencing information, the following occurs:</span></span>

-   <span data-ttu-id="97904-108">В [таблицу мсипатчсекуенце](msipatchsequence-table.md) добавляется новая строка для каждого кода продукта целевого образа, который указан в [таблице таржетимажес](targetimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="97904-108">A new row is added to the [MsiPatchSequence Table](msipatchsequence-table.md) for each product code of a target image that is listed in the [TargetImages Table](targetimages-table-patchwiz-dll-.md).</span></span>
-   <span data-ttu-id="97904-109">Значения, добавляемые в столбец Патчфамили в новых строках, соответствуют целевым кодам продуктов целевых изображений, перечисленным в [таблице таржетимажес](targetimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="97904-109">The values added to the PatchFamily column in the new rows correspond to the target product codes of the target images that are listed in the [TargetImages Table](targetimages-table-patchwiz-dll-.md).</span></span>
-   <span data-ttu-id="97904-110">Значения, добавляемые к столбцам последовательности в новых строках, создаются с использованием самой высокой версии продукта, предназначенной для исправления, и времени в формате UTC при создании исправления.</span><span class="sxs-lookup"><span data-stu-id="97904-110">The values added to the Sequence columns in the new rows are generated using the highest product version targeted by the patch and the UTC time when the patch is generated.</span></span> <span data-ttu-id="97904-111">Порядковый номер: <Product Minor Version> . <Build Major Number> . <метка времени 1>. <метка времени 2>.</span><span class="sxs-lookup"><span data-stu-id="97904-111">The sequence number is <Product Minor Version>.<Build Major Number>.<Time Stamp 1>.<Time Stamp 2>.</span></span>
    -   <span data-ttu-id="97904-112">Первое поле — это версия продукта самой высокой версии продукта, для которой предназначено исправление.</span><span class="sxs-lookup"><span data-stu-id="97904-112">The first field is the product version of the highest version of the product that is targeted by the patch.</span></span>
    -   <span data-ttu-id="97904-113">Второе поле — это основной номер версии продукта, который является целью исправления.</span><span class="sxs-lookup"><span data-stu-id="97904-113">The second field is the build major number of the highest version of the product that is targeted by the patch.</span></span>

    <span data-ttu-id="97904-114">Два поля метки времени имеют отметку времени 32 бит, необходимую для подсчета секунд в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="97904-114">The two time stamp fields account for the 32 bit time stamp that is needed to count the seconds in Coordinated Universal Time (UTC).</span></span>
    > [!Note]  
    > <span data-ttu-id="97904-115">Версии продукта имеют следующий формат: <Product Major Version> . <Product Minor Version> . <Build Major Number> . <Build Minor Number> и продукт с номером версии 2.1.0.0 имеет более позднюю версию, чем продукт с номером версии 1.2.0.0</span><span class="sxs-lookup"><span data-stu-id="97904-115">Product versions have the following format: <Product Major Version>.<Product Minor Version>.<Build Major Number>.<Build Minor Number> and a product with a version number 2.1.0.0 is a higher version than a product with version number 1.2.0.0</span></span>

     

-   <span data-ttu-id="97904-116">Атрибут Мсидбпатчсекуенцесуперседиарлиер введен в столбец атрибутов новых строк, созданных для пакетов обновления (SP) или незначительных обновлений.</span><span class="sxs-lookup"><span data-stu-id="97904-116">The msidbPatchSequenceSupersedeEarlier attribute is entered into the Attribute column of new rows that are generated for service packs (SP) or minor upgrade patches.</span></span> <span data-ttu-id="97904-117">Атрибут Мсидбпатчсекуенцесуперседиарлиер не добавляется в исправление QFE или небольшое обновление.</span><span class="sxs-lookup"><span data-stu-id="97904-117">The msidbPatchSequenceSupersedeEarlier attribute is not added to a QFE or small update patch.</span></span>
    > [!Note]  
    > <span data-ttu-id="97904-118">Пакет обновления (SP) должен содержать исправления всех QFE, выпущенных до этой версии.</span><span class="sxs-lookup"><span data-stu-id="97904-118">A service pack (SP) should contain the fixes of all the QFEs that were released prior to it.</span></span> <span data-ttu-id="97904-119">Однако если автор исправления устанавливает для \_ свойства замена данных последовательности \_ значение 0 (ноль) или 1 (один) в PCP-файле, то столбцу Attributes всех строк в таблице мсипатчсекуенце присваивается значение, указанное для \_ замены данных последовательности \_ .</span><span class="sxs-lookup"><span data-stu-id="97904-119">However, if a patch author sets the SEQUENCE\_DATA\_SUPERSEDENCE property to 0 (zero) or 1 (one) in the .pcp file, the Attributes column of all rows in the MsiPatchSequence table is set to the value that is specified for SEQUENCE\_DATA\_SUPERSEDENCE.</span></span> <span data-ttu-id="97904-120">Авторы исправлений, которым требуется больший контроль, должны вручную создать столбец Attributes.</span><span class="sxs-lookup"><span data-stu-id="97904-120">Patch authors who require more control must author the Attributes column manually.</span></span>

     

<span data-ttu-id="97904-121">Если включить [таблицу патчсекуенце](patchsequence-table--patchwiz-dll-.md) в PCP-файл, \_ \_ свойство отключение создания данных последовательностей \_ игнорируется, а сведения, содержащиеся в таблице Патчсекуенце, можно добавить в [таблицу мсипатчсекуенце](msipatchsequence-table.md) обновления.</span><span class="sxs-lookup"><span data-stu-id="97904-121">If you include a [PatchSequence Table](patchsequence-table--patchwiz-dll-.md) in the .pcp file, the SEQUENCE\_DATA\_GENERATION\_DISABLED property is ignored and the information provided in the PatchSequence Table can be added to the [MsiPatchSequence Table](msipatchsequence-table.md) of the patch.</span></span>

 

 



