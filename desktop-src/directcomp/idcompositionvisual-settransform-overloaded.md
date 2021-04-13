---
title: Методы Сеттрансформ Идкомпоситионвисуал (Дкомп. h)
description: Задает свойство Transform этого визуального элемента. Свойство Transform указывает 2D-преобразование, используемое для изменения системы координат данного визуального элемента. Свойство может задавать матрицу преобразования размером 3 на 2 или объект преобразования.
ms.assetid: DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D
keywords:
- Методы Сеттрансформ DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 00f5da890cd22c5c827a36062a0b0c3f9bc19cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341165"
---
# <a name="idcompositionvisualsettransform-methods"></a>Методы Идкомпоситионвисуал:: Сеттрансформ

Задает свойство Transform этого визуального элемента. Свойство Transform указывает 2D-преобразование, используемое для изменения системы координат данного визуального элемента. Свойство может задавать матрицу преобразования размером 3 на 2 или объект преобразования.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                    | Описание                                                                    |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Сеттрансформ ( \_ Матрица D2D \_ 3X2 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))          | Устанавливает свойство Transform в указанную матрицу преобразования.<br/>      |
| [**Сеттрансформ (Идкомпоситионтрансформ \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform)) | Задает для свойства Transform указанный объект преобразования.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Дкомп. h</dt> </dl>   |
| Библиотека<br/>                  | <dl> <dt>Дкомп. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Dcomp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**идкомпоситионматрикстрансформ**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[**идкомпоситионротатетрансформ**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[**идкомпоситионскалетрансформ**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[**идкомпоситионскевтрансформ**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[**идкомпоситионтрансформ**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[**идкомпоситионтранслатетрансформ**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[**идкомпоситионвисуал**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[**Идкомпоситионвисуал:: Сетоффсеткс**](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[**Идкомпоситионвисуал:: Сетоффсети**](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

�

�
