---
title: Идентификаторы типов цветового пространства
description: Эти константы определяют тип массива цветового пространства PostScript 2. Следующие значения являются допустимыми типами массивов цветового пространства.
ms.assetid: dc312db2-3bc5-461f-819c-37ff14cff896
topic_type:
- apiref
api_name:
- CSA_A
- CSA_GRAY
- CSA_ABC
- CSA_DEF
- CSA_RGB
- CSA_Lab
- CSA_DEFG
- CSA_CMYK
api_type:
- NA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 973db6c56dda5bde8614dffa13f461761934fcde
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/02/2021
ms.locfileid: "105719855"
---
# <a name="color-space-type-identifiers"></a>Идентификаторы типов цветового пространства

Эти константы определяют тип массива цветового пространства PostScript 2. Следующие значения являются допустимыми типами массивов цветового пространства.

<dl> <dt>

<span id="CSA_A"></span><span id="csa_a"></span>**CSA \_ A**
</dt> <dd> <dl> <dt>



Получите массив цветового пространства Циебаседа из монохромного профиля.


</dt> </dl> </dd> <dt>

<span id="CSA_GRAY"></span><span id="csa_gray"></span>**\_СЕРАЯ CSA**
</dt> <dd> <dl> <dt>



Получите массив цветового пространства Циебаседа из монохромного профиля.


</dt> </dl> </dd> <dt>

<span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA \_ ABC**
</dt> <dd> <dl> <dt>



Получите массив цветовых пространств Циебаседабк из профиля RGB или L <sup>\*</sup> a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_DEF"></span><span id="csa_def"></span>**CSA \_ DEF**
</dt> <dd> <dl> <dt>



Получите массив цветовых пространств Циебаседдеф из профиля RGB или L <sup>\*</sup> a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_RGB"></span><span id="csa_rgb"></span>**CSA \_ RGB**
</dt> <dd> <dl> <dt>



Получите массив цветового пространства Циебаседдеф, за которым следует массив цветового пространства Циебаседабк из профиля RGB. При выполнении, если принтер не поддерживает Циебаседдеф цветовые пространства, функция использует определение Циебаседабк.


</dt> </dl> </dd> <dt>

<span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**CSA \_ Labs**
</dt> <dd> <dl> <dt>



Возвращает массив цветового пространства Циебаседабк из профиля L <sup>\*</sup> a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_DEFG"></span><span id="csa_defg"></span>**CSA \_ дефг**
</dt> <dd> <dl> <dt>



Получите массив цветовых пространств Циебаседдефг из профиля CMYK.


</dt> </dl> </dd> <dt>

<span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA \_ CMYK**
</dt> <dd> <dl> <dt>



Получите массив цветовых пространств Циебаседкмик из профиля CMYK.


</dt> </dl> </dd> </dl>

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Основные понятия управления цветом](basic-color-management-concepts.md)
</dt> <dt>

[Константы ICM](wcs-constants.md)
</dt> </dl>

 

 




