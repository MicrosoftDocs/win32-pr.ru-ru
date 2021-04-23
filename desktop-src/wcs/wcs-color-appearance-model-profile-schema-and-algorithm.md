---
title: Схема и алгоритм профиля модели цветового оформления WCS
description: Схема и алгоритм профиля модели цветового оформления WCS
ms.assetid: 017588fe-cec9-4178-a912-7950cefc036c
keywords:
- Цветовая система Windows (WCS), профиль модели цветового оформления (CAMP)
- WCS (цветовая система Windows), профиль модели цветового оформления (CAMP)
- Управление цветом изображений, профиль модели цветового оформления (CAMP)
- Управление цветом, профиль модели цветового оформления (CAMP)
- цвет, профиль модели цветового оформления (CAMP)
- Цветовая система Windows (WCS), профили
- WCS (цветовая система Windows), профили
- Управление цветом изображений, профили
- Управление цветом, профили
- цвета, профили
- Профиль модели цветового оформления (CAMP)
- CAMP (профиль модели цветового оформления)
- схемы, профиль модели цветового оформления (CAMP)
- алгоритмы, профиль модели цветового оформления (CAMP)
- Профиль модели цветового оформления WCS
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a928aebcfe02f1db39de2452a0b49e5c888bccc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "105719871"
---
# <a name="wcs-color-appearance-model-profile-schema-and-algorithm"></a><span data-ttu-id="5645e-118">Схема и алгоритм профиля модели цветового оформления WCS</span><span class="sxs-lookup"><span data-stu-id="5645e-118">WCS Color Appearance Model Profile Schema and Algorithm</span></span>

[<span data-ttu-id="5645e-119">Обзор</span><span class="sxs-lookup"><span data-stu-id="5645e-119">Overview</span></span>](#overview)

[<span data-ttu-id="5645e-120">Архитектура профиля модели цветового оформления (CAMP)</span><span class="sxs-lookup"><span data-stu-id="5645e-120">Color Appearance Model Profile (CAMP) Architecture</span></span>](#color-appearance-model-profile-architecture)

[<span data-ttu-id="5645e-121">Схема CAMP</span><span class="sxs-lookup"><span data-stu-id="5645e-121">The CAMP Schema</span></span>](#the-camp-schema)

[<span data-ttu-id="5645e-122">Элементы схемы CAMP</span><span class="sxs-lookup"><span data-stu-id="5645e-122">The CAMP Schema Elements</span></span>](#the-camp-schema-elements)

[<span data-ttu-id="5645e-123">Алгоритм CAMP</span><span class="sxs-lookup"><span data-stu-id="5645e-123">The CAMP Algorithm</span></span>](#the-camp-algorithm)

### <a name="overview"></a><span data-ttu-id="5645e-124">Обзор</span><span class="sxs-lookup"><span data-stu-id="5645e-124">Overview</span></span>

<span data-ttu-id="5645e-125">Эта схема используется для указания содержимого профиля модели цветового представления (CAMP).</span><span class="sxs-lookup"><span data-stu-id="5645e-125">This schema is used to specify the content of a color appearance model profile (CAMP).</span></span> <span data-ttu-id="5645e-126">Связанные базовые алгоритмы описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="5645e-126">The associated baseline algorithms are described in the following sections.</span></span>

<span data-ttu-id="5645e-127">CAMP состоит из XML-тегов, которые предоставляют переменные значения для переменных модели внешнего вида CIECAM02 базового цвета.</span><span class="sxs-lookup"><span data-stu-id="5645e-127">The CAMP is composed of XML tags that provide parametric values to the CIECAM02 baseline color appearance model variables.</span></span> <span data-ttu-id="5645e-128">Сведения о диапазонах для параметров приведены в спецификации модели определения основного цвета и рекомендации по CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="5645e-128">Details on the ranges for parameters are provided in the baseline color appearance model specification and CIECAM02 recommendation.</span></span>

### <a name="color-appearance-model-profile-architecture"></a><span data-ttu-id="5645e-129">Архитектура профиля модели цветового отображения</span><span class="sxs-lookup"><span data-stu-id="5645e-129">Color Appearance Model Profile Architecture</span></span>

![Схема, на которой показана архитектура профиля CAMP, созданная с помощью тегов X M L.](images/camp-image002new.png)

### <a name="the-camp-schema"></a><span data-ttu-id="5645e-131">Схема CAMP</span><span class="sxs-lookup"><span data-stu-id="5645e-131">The CAMP Schema</span></span>


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema
  xmlns:cam="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Appearance Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:annotation>
    <xs:documentation>
      ColorAppearanceModel element contains viewing conditions
      parameters based on CIECAM02.
    </xs:documentation>
  </xs:annotation>
  <xs:element name="ColorAppearanceModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="ViewingConditions">
          <xs:complexType>
            <xs:sequence>
              <xs:choice>
                <xs:element name="WhitePoint" type="wcs:NonNegativeCIEXYZType"/>
                <xs:element name="WhitePointName">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="D50"/>
                      <xs:enumeration value="D65"/>
                      <xs:enumeration value="A"/>
                      <xs:enumeration value="F2"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:element>
              </xs:choice>
              <xs:element name="Background" type="wcs:NonNegativeCIEXYZType"/>
              <xs:choice>
                <xs:element name="ImpactOfSurround" type="xs:float"/>
                <xs:element name="Surround">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="Average"/>
                      <xs:enumeration value="Dim"/>
                      <xs:enumeration value="Dark"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:element>
              </xs:choice>
              <xs:element name="LuminanceOfAdaptingField" type="xs:float"/>
              <xs:element name="DegreeOfAdaptation" type="xs:float"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
        <xs:element name="NormalizeToMediaWhitePoint" minOccurs="0">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="True"/>
              <xs:enumeration value="False"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>
```



## <a name="the-camp-schema-elements"></a><span data-ttu-id="5645e-132">Элементы схемы CAMP</span><span class="sxs-lookup"><span data-stu-id="5645e-132">The CAMP Schema Elements</span></span>

## <a name="colorappearancemodel"></a><span data-ttu-id="5645e-133">колораппеаранцемодел</span><span class="sxs-lookup"><span data-stu-id="5645e-133">ColorAppearanceModel</span></span>

<span data-ttu-id="5645e-134">Этот элемент является последовательностью:</span><span class="sxs-lookup"><span data-stu-id="5645e-134">This element is a sequence of:</span></span>

1.  <span data-ttu-id="5645e-135">Строка имени файла,</span><span class="sxs-lookup"><span data-stu-id="5645e-135">ProfileName string,</span></span>
2.  <span data-ttu-id="5645e-136">Необязательная строка описания</span><span class="sxs-lookup"><span data-stu-id="5645e-136">optional Description string,</span></span>
3.  <span data-ttu-id="5645e-137">Необязательная строка автора</span><span class="sxs-lookup"><span data-stu-id="5645e-137">optional Author string,</span></span>
4.  <span data-ttu-id="5645e-138">Элемент Виевингкондитионс.</span><span class="sxs-lookup"><span data-stu-id="5645e-138">ViewingConditions element.</span></span>

<span data-ttu-id="5645e-139">**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.</span><span class="sxs-lookup"><span data-stu-id="5645e-139">**Validation conditions:** Each sub-element is validated by its own type.</span></span> <span data-ttu-id="5645e-140">Длина строк ограничена 10 000 символами.</span><span class="sxs-lookup"><span data-stu-id="5645e-140">String lengths are limited to 10,000 characters.</span></span>

## <a name="namespace"></a><span data-ttu-id="5645e-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5645e-141">Namespace</span></span>

<span data-ttu-id="5645e-142">xmlns: Камера = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "</span><span class="sxs-lookup"><span data-stu-id="5645e-142">xmlns:cam="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"</span></span>

<span data-ttu-id="5645e-143">targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "</span><span class="sxs-lookup"><span data-stu-id="5645e-143">targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"</span></span>

## <a name="version"></a><span data-ttu-id="5645e-144">Версия</span><span class="sxs-lookup"><span data-stu-id="5645e-144">Version</span></span>

<span data-ttu-id="5645e-145">Версия &gt; 0,1 или &lt; = "1,0" с первым выпуском Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5645e-145">Version &gt;0.1 or &lt;= "1.0" with the first release of Windows Vista.</span></span>

<span data-ttu-id="5645e-146">**Условия проверки:** Любое значение версии &lt; = 2,0 также допустимо для поддержки некритических изменений в формате.</span><span class="sxs-lookup"><span data-stu-id="5645e-146">**Validation conditions:** Any version value &lt;=2.0 is also valid to support non-breaking changes to the format.</span></span>

## <a name="documentation"></a><span data-ttu-id="5645e-147">Документация</span><span class="sxs-lookup"><span data-stu-id="5645e-147">Documentation</span></span>

<span data-ttu-id="5645e-148">Схема профиля модели цветового оформления.</span><span class="sxs-lookup"><span data-stu-id="5645e-148">Color Appearance Model Profile Schema.</span></span>

<span data-ttu-id="5645e-149">(C) корпорация Майкрософт (Microsoft Corporation).</span><span class="sxs-lookup"><span data-stu-id="5645e-149">Copyright (C) Microsoft.</span></span> <span data-ttu-id="5645e-150">Все права защищены.</span><span class="sxs-lookup"><span data-stu-id="5645e-150">All rights reserved.</span></span>

<span data-ttu-id="5645e-151">**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.</span><span class="sxs-lookup"><span data-stu-id="5645e-151">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

## <a name="surroundtype"></a><span data-ttu-id="5645e-152">сурраундтипе</span><span class="sxs-lookup"><span data-stu-id="5645e-152">SurroundType</span></span>

<span data-ttu-id="5645e-153">Этот элемент является либо перечислением "среднего", "Dim", либо "темного" параметров CIECAM02, либо фактическим количественным параметром из рекомендации CIECAM02 c, влиянием окружающего элемента.</span><span class="sxs-lookup"><span data-stu-id="5645e-153">This element is a either an enumeration of "Average," "Dim," or "Dark" CIECAM02 parameters or the actual quantitative parameters from the CIECAM02 recommendation c, impact of the surround.</span></span>

<span data-ttu-id="5645e-154">**Условия проверки:** Параметр c может находиться в диапазоне от 0,525 до 0,69.</span><span class="sxs-lookup"><span data-stu-id="5645e-154">**Validation conditions:** The c parameter can range from 0.525 to 0.69.</span></span>

## <a name="viewingconditions"></a><span data-ttu-id="5645e-155">виевингкондитионс</span><span class="sxs-lookup"><span data-stu-id="5645e-155">ViewingConditions</span></span>

<span data-ttu-id="5645e-156">Этот элемент состоит из следующих вложенных элементов:</span><span class="sxs-lookup"><span data-stu-id="5645e-156">This element consists of the following sub-elements:</span></span>



| <span data-ttu-id="5645e-157">Элемент</span><span class="sxs-lookup"><span data-stu-id="5645e-157">Element</span></span>                    | <span data-ttu-id="5645e-158">Тип</span><span class="sxs-lookup"><span data-stu-id="5645e-158">Type</span></span>           |
|----------------------------|----------------|
| <span data-ttu-id="5645e-159">вхитепоинт</span><span class="sxs-lookup"><span data-stu-id="5645e-159">WhitePoint</span></span>                 | <span data-ttu-id="5645e-160">вхитепоинттипе</span><span class="sxs-lookup"><span data-stu-id="5645e-160">WhitePointType</span></span> |
| <span data-ttu-id="5645e-161">Историческая справка</span><span class="sxs-lookup"><span data-stu-id="5645e-161">Background</span></span>                 | <span data-ttu-id="5645e-162">Циексиз</span><span class="sxs-lookup"><span data-stu-id="5645e-162">CIEXYZ</span></span>         |
| <span data-ttu-id="5645e-163">Окружа</span><span class="sxs-lookup"><span data-stu-id="5645e-163">Surround</span></span>                   | <span data-ttu-id="5645e-164">сурраундтипе</span><span class="sxs-lookup"><span data-stu-id="5645e-164">SurroundType</span></span>   |
| <span data-ttu-id="5645e-165">луминанцеофадаптингфиелд</span><span class="sxs-lookup"><span data-stu-id="5645e-165">LuminanceOfAdaptingField</span></span>   | <span data-ttu-id="5645e-166">FLOAT</span><span class="sxs-lookup"><span data-stu-id="5645e-166">float</span></span>          |
| <span data-ttu-id="5645e-167">дегриофадаптатион</span><span class="sxs-lookup"><span data-stu-id="5645e-167">DegreeOfAdaptation</span></span>         | <span data-ttu-id="5645e-168">FLOAT</span><span class="sxs-lookup"><span data-stu-id="5645e-168">float</span></span>          |
| <span data-ttu-id="5645e-169">нормализетомедиавхитепоинт</span><span class="sxs-lookup"><span data-stu-id="5645e-169">NormalizeToMediaWhitePoint</span></span> | <span data-ttu-id="5645e-170">Логическое</span><span class="sxs-lookup"><span data-stu-id="5645e-170">Boolean</span></span>        |



 

<span data-ttu-id="5645e-171">**Условия проверки:** Вложенные элементы ЦИЕКСИЗ проверяются с помощью Ноннегативексизтипе.</span><span class="sxs-lookup"><span data-stu-id="5645e-171">**Validation conditions:** CIEXYZ sub-elements are validated by NonNegativeXYZType.</span></span> <span data-ttu-id="5645e-172">Луминанцеофадаптингфиелд имеет максимум 10, 000cd/m ^ 2.</span><span class="sxs-lookup"><span data-stu-id="5645e-172">The LuminanceOfAdaptingField is a maximum of 10,000cd/m^2.</span></span> <span data-ttu-id="5645e-173">Дегриофадаптатион может находиться в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="5645e-173">The DegreeOfAdaptation can range from 0.0 to 1.0.</span></span> <span data-ttu-id="5645e-174">Значение Нормализетомедиавхитепоинт может быть либо "true", либо "false".</span><span class="sxs-lookup"><span data-stu-id="5645e-174">The NormalizeToMediaWhitePoint value can be either "true" or "false."</span></span> <span data-ttu-id="5645e-175">Если вложенный элемент Нормализетомедиавхитепоинт отсутствует, по умолчанию он имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="5645e-175">If the NormalizeToMediaWhitePoint sub-element is absent, it effectively defaults to "true."</span></span> <span data-ttu-id="5645e-176">См. подраздел о следующем алгоритме CAMP.</span><span class="sxs-lookup"><span data-stu-id="5645e-176">See the following CAMP algorithm section.</span></span>

## <a name="whitepointtype"></a><span data-ttu-id="5645e-177">вхитепоинттипе</span><span class="sxs-lookup"><span data-stu-id="5645e-177">WhitePointType</span></span>

<span data-ttu-id="5645e-178">Этот элемент является либо перечислением ЦИЕ источника освещения ("D50", "D65", "A," или "F2"), либо вложенным элементом ЦИЕКСИЗ.</span><span class="sxs-lookup"><span data-stu-id="5645e-178">This element is a either an enumeration of CIE light source value ("D50," "D65," "A," or "F2") or a CIEXYZ sub-element.</span></span>

<span data-ttu-id="5645e-179">**Условия проверки:** Каждый вложенный элемент проверяется по собственному типу.</span><span class="sxs-lookup"><span data-stu-id="5645e-179">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

## <a name="ciexyztype"></a><span data-ttu-id="5645e-180">Циексизтипе</span><span class="sxs-lookup"><span data-stu-id="5645e-180">CIEXYZType</span></span>

<span data-ttu-id="5645e-181">Элемент Циексизтипе состоит из трех Ноннегативефлоаттипеных элементов с плавающей запятой одиночной точности с именами "X", "Y" и "Z".</span><span class="sxs-lookup"><span data-stu-id="5645e-181">The CIEXYZType element is composed of three NonNegativeFloatType single-precision IEEE floating-point elements, named "X," "Y," and "Z."</span></span> <span data-ttu-id="5645e-182">Эти измерения могут быть абсолютными (не относительными) ЦИЕКСИЗ 1931 отражающими значениями или абсолютными (не относительными) ЦИЕКСИЗ 1931 прямыми (передаваемые) значениями в Канделас на единицы измерения с квадратом.</span><span class="sxs-lookup"><span data-stu-id="5645e-182">These measurements can be either absolute (not relative) CIEXYZ 1931 reflective values or absolute (not relative) CIEXYZ 1931 direct (transmissive) values in candelas per meter squared units.</span></span>

<span data-ttu-id="5645e-183">**Условия проверки:** Это означает, что допустимы только реальные значения, а отрицательные значения измерения ЦИЕКСИЗ недопустимы.</span><span class="sxs-lookup"><span data-stu-id="5645e-183">**Validation conditions:** This means that only real-world values are valid, and negative CIEXYZ measurement values are invalid.</span></span> <span data-ttu-id="5645e-184">Так как эти значения являются абсолютными, значения могут иметь более широкий диапазон, чем 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="5645e-184">Since these are absolute values, values can range well beyond 1.0f.</span></span> <span data-ttu-id="5645e-185">Разумное ограничение для любого значения X, Y или Z будет произвольно установлено в 10000.0 f.</span><span class="sxs-lookup"><span data-stu-id="5645e-185">A reasonable limit for any X, Y, or Z value will be arbitrarily set to 10000.0f.</span></span>

 

### <a name="the-camp-algorithm"></a><span data-ttu-id="5645e-186">Алгоритм CAMP</span><span class="sxs-lookup"><span data-stu-id="5645e-186">The CAMP Algorithm</span></span>

<span data-ttu-id="5645e-187">Модель цветового оформления (камера) основана на уравнениях модели отображения цвета ЦИЕ CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="5645e-187">The color appearance model (CAM) is based on the CIE CIECAM02 color appearance model equations.</span></span>

<span data-ttu-id="5645e-188">Этот класс реализует моделирование цветового представления.</span><span class="sxs-lookup"><span data-stu-id="5645e-188">This class implements the color appearance modeling.</span></span> <span data-ttu-id="5645e-189">Обратите внимание, что камера WCS *не может быть* заменяемой, например, с помощью подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="5645e-189">Note that the WCS CAM is *not* replaceable, for example, using a plug-in.</span></span> <span data-ttu-id="5645e-190">Задача разработки должна иметь только одну модель отображения цвета.</span><span class="sxs-lookup"><span data-stu-id="5645e-190">It is a design goal to have only one color appearance model.</span></span> <span data-ttu-id="5645e-191">Камера основана на рекомендациях CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="5645e-191">The CAM is based on CIECAM02 recommendations.</span></span>

<span data-ttu-id="5645e-192">CIECAM02 можно использовать двумя способами.</span><span class="sxs-lookup"><span data-stu-id="5645e-192">CIECAM02 can be used in two ways.</span></span> <span data-ttu-id="5645e-193">В направлении «от + до-отображения» оно обеспечивает сопоставление пространства ЦИЕ XYZ с цветом.</span><span class="sxs-lookup"><span data-stu-id="5645e-193">In the colorimetric-to-appearance direction, it provides a mapping from CIE XYZ space to color appearance space.</span></span> <span data-ttu-id="5645e-194">В направлении, сопоставленном с цветами, оно преобразуется обратно в пространство XYZ.</span><span class="sxs-lookup"><span data-stu-id="5645e-194">In the appearance-to-colorimetric direction, it maps from color appearance space back to XYZ space.</span></span> <span data-ttu-id="5645e-195">Цветовой стиль соответствует освещениям, J, чрома, C и оттенок, h.</span><span class="sxs-lookup"><span data-stu-id="5645e-195">The color appearance correlates lightness, J, chroma, C, and hue, h.</span></span> <span data-ttu-id="5645e-196">Эти три значения образуют цилиндрическую систему координат.</span><span class="sxs-lookup"><span data-stu-id="5645e-196">These three values form a cylindrical coordinate system.</span></span> <span data-ttu-id="5645e-197">Часто бывает удобнее работать в прямоугольной системе координат, поэтому вычислить a = C COS h и b = C Sin h, чтобы предоставить CIECAM02 Jab.</span><span class="sxs-lookup"><span data-stu-id="5645e-197">Frequently, it turns out to be more convenient to work in a rectangular coordinate system, so compute a = C cos h and b = C sin h, to give CIECAM02 Jab.</span></span>

<span data-ttu-id="5645e-198">Можно использовать значения яркости, превышающие 100.</span><span class="sxs-lookup"><span data-stu-id="5645e-198">You can use CAM lightness values greater than 100.</span></span> <span data-ttu-id="5645e-199">Комитет ЦИЕ, который настроил CIECAM02, не содержал поведение оси освещенности для входных значений с яркостью выше принятой белой точки; то есть, для входных значений Y больше, чем принятое значение Y белой точки.</span><span class="sxs-lookup"><span data-stu-id="5645e-199">The CIE committee that formulated CIECAM02 did not address the behavior of the lightness axis for input values with a luminance greater than the adopted white point; that is, for input Y values greater than the adopted white point Y value.</span></span> <span data-ttu-id="5645e-200">Эксперимент показывает, что уравнения светимости в CIECAM02 ведут себя так, как такие значения.</span><span class="sxs-lookup"><span data-stu-id="5645e-200">Experimentation has shown that the luminance equations in CIECAM02 behave reasonably for such values.</span></span> <span data-ttu-id="5645e-201">Освещение увеличивается экспоненциально и следует за тем же экспонентой (примерно 1/3).</span><span class="sxs-lookup"><span data-stu-id="5645e-201">The lightness increases exponentially and follows the same exponent (roughly 1/3).</span></span>

<span data-ttu-id="5645e-202">Иногда пользователям нужно изменить способ вычисления степени адаптации (D).</span><span class="sxs-lookup"><span data-stu-id="5645e-202">Users sometimes want to change the way that the degree of adaptation (D) is calculated.</span></span> <span data-ttu-id="5645e-203">Структура WCS позволяет пользователям управлять этим вычислением, изменяя значение Дегриофадаптатион в параметрах условий просмотра.</span><span class="sxs-lookup"><span data-stu-id="5645e-203">The WCS design enables users to control this calculation by changing the degreeOfadaptation value in the viewing conditions parameters.</span></span>

<span data-ttu-id="5645e-204">Чтобы обеспечить более согласованное соответствие требованиям ICC пользователей к ожиданиям, Дегриофадаптатион в Camp по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="5645e-204">To provide a more consistent match to users' ICC-influenced expectations, the degreeOfAdaptation in the default CAMPS is 1.0.</span></span> <span data-ttu-id="5645e-205">Это дает лучшие результаты во всех случаях, кроме Минкд Absolute, где может потребоваться разрешить WCS вычислить Дегриофадаптатион (через Дегриофадаптатион =-1).</span><span class="sxs-lookup"><span data-stu-id="5645e-205">This produces better results in all cases other than MinCD Absolute, where one might want to let WCS compute the degreeOfAdaptation (via degreeOfAdaptation = -1).</span></span>

<span data-ttu-id="5645e-206">Вместо использования окружающего значения "среднее", "Dim" и "темное" предоставляется непрерывное значение, вычисленное на основе значения c.</span><span class="sxs-lookup"><span data-stu-id="5645e-206">Instead of using a surround value of "Average," "Dim," and "Dark," a continuous surround value, computed from the value c, is provided.</span></span> <span data-ttu-id="5645e-207">Значение c должно быть числом в диапазоне от 0,525 до 0,69.</span><span class="sxs-lookup"><span data-stu-id="5645e-207">The value of c must be a float between 0.525 and 0.69.</span></span>

<span data-ttu-id="5645e-208">Из *c*, *NC* и *F* можно вычислить, используя линейную интерполяцию кусочно-между значениями, которые уже предоставлены для "среднего", "Dim" и "темного".</span><span class="sxs-lookup"><span data-stu-id="5645e-208">From *c*, *Nc* and *F* can be computed, using piecewise linear interpolation between the values already provided for "Average," "Dim," and "Dark."</span></span> <span data-ttu-id="5645e-209">Эта модель показывает, что показано на рисунке 1 ЦИЕ 159:2004, спецификации CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="5645e-209">This models what is shown in Figure 1 of CIE 159:2004, the CIECAM02 specification.</span></span>



| <span data-ttu-id="5645e-210">дегриофадаптион</span><span class="sxs-lookup"><span data-stu-id="5645e-210">degreeOfAdaption</span></span>                     | <span data-ttu-id="5645e-211">Поведение</span><span class="sxs-lookup"><span data-stu-id="5645e-211">Behavior</span></span>                                                                       |
|--------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="5645e-212">-1.0</span><span class="sxs-lookup"><span data-stu-id="5645e-212">-1.0</span></span>                                 | ![Показывает формулу для поведения по умолчанию C I E C и M 02.](images/camp-image006.png)<span data-ttu-id="5645e-214">Это поведение CIECAM02 по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5645e-214">This is the default CIECAM02 behavior.</span></span><br/> |
| <span data-ttu-id="5645e-215">0,0 &lt; = дегриофадаптион &lt; = 1,0</span><span class="sxs-lookup"><span data-stu-id="5645e-215">0.0 &lt;= degreeOfAdaption &lt;= 1.0</span></span> | <span data-ttu-id="5645e-216">*D* = дегриофадаптатион (значение, предоставленное пользователем)</span><span class="sxs-lookup"><span data-stu-id="5645e-216">*D* = degreeOfAdaptation (the value supplied by the user)</span></span>                      |



 

<span data-ttu-id="5645e-217">В реализацию также добавлен определенный объем проверки ошибок.</span><span class="sxs-lookup"><span data-stu-id="5645e-217">A certain amount of error checking has also been added to the implementation.</span></span> <span data-ttu-id="5645e-218">Следующие числа уравнений используются в определении ЦИЕ 159:2004 CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="5645e-218">The following equation numbers are those used in the CIE 159:2004 definition of CIECAM02.</span></span>

<span data-ttu-id="5645e-219">**колориметриктоаппеаранцеколорс**</span><span class="sxs-lookup"><span data-stu-id="5645e-219">**ColorimetricToAppearanceColors**</span></span>

<span data-ttu-id="5645e-220">Входные значения проверяются на разумность: если X или Z &lt; 0,0 или Y &lt; -1,0, то значением HRESULT является E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="5645e-220">The input values are checked for reasonableness: If X or Z &lt; 0.0, or if Y &lt; -1.0, then the HRESULT is E\_INVALIDARG.</span></span> <span data-ttu-id="5645e-221">Если-1,0 &lt; = Y &lt; 0,0, то для J, C и h устанавливается значение 0,0.</span><span class="sxs-lookup"><span data-stu-id="5645e-221">If -1.0 &lt;= Y &lt; 0.0, then J, C, and h are all set to 0.0.</span></span>

<span data-ttu-id="5645e-222">Существуют определенные внутренние условия, которые могут выдавать результаты ошибки.</span><span class="sxs-lookup"><span data-stu-id="5645e-222">There are certain internal conditions that can produce error results.</span></span> <span data-ttu-id="5645e-223">Вместо создания таких результатов внутренние результаты обрезаются для получения значений в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="5645e-223">Instead of producing such results, the internal results are clipped to produce in-range values.</span></span> <span data-ttu-id="5645e-224">Это происходит для спецификаций цветов, которые были бы темными и невероятными: в уравнении 7,23, если &lt; 0, a = 0.</span><span class="sxs-lookup"><span data-stu-id="5645e-224">This happens for specifications of colors that would be dark and impossibly chromatic: In equation 7.23, if A &lt; 0, A = 0.</span></span> <span data-ttu-id="5645e-225">В уравнении 7,26, если t &lt; 0, t = 0.</span><span class="sxs-lookup"><span data-stu-id="5645e-225">In equation 7.26, if t &lt; 0, t = 0.</span></span>

<span data-ttu-id="5645e-226">**аппеаранцетоколориметрикколорс**</span><span class="sxs-lookup"><span data-stu-id="5645e-226">**AppearanceToColorimetricColors**</span></span>

<span data-ttu-id="5645e-227">Входные значения проверяются на разумность.</span><span class="sxs-lookup"><span data-stu-id="5645e-227">The input values are checked for reasonableness.</span></span> <span data-ttu-id="5645e-228">Если C &lt; 0, c &gt; 300 или J &gt; 500, то значением HRESULT является E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="5645e-228">If C &lt; 0 , C &gt; 300, or J &gt; 500, then the HRESULT is E\_INVALIDARG.</span></span>

<span data-ttu-id="5645e-229">*R "<sub>a;</sub>*, *G"<sub>a;</sub>* и *B "<sub>a;</sub>*(уравнения 8,19-8,21) обрезаются до диапазона 399,9.</span><span class="sxs-lookup"><span data-stu-id="5645e-229">*R'<sub>a;</sub>*, *G'<sub>a;</sub>*, and *B'<sub>a;</sub>*, (equations 8.19 - 8.21) are clipped to the range   399.9 .</span></span>

<span data-ttu-id="5645e-230">Для всех профилей модели цветового оформления (Camp) подсистема WCS будет проверять принятые белые точки.</span><span class="sxs-lookup"><span data-stu-id="5645e-230">For all Color Appearance Model Profiles (CAMPs), the WCS engine will examine the adopted white point.</span></span> <span data-ttu-id="5645e-231">Если значение Y не равно 100,0, то принятая белая точка будет масштабироваться таким образом, что Y равняется 100,0.</span><span class="sxs-lookup"><span data-stu-id="5645e-231">If Y is not 100.0, then the adopted white point will be scaled so that Y does equal 100.0.</span></span> <span data-ttu-id="5645e-232">То же масштабирование будет применено к значению фона.</span><span class="sxs-lookup"><span data-stu-id="5645e-232">The same scaling will be applied to the background value.</span></span> <span data-ttu-id="5645e-233">Коэффициент масштабирования — 100,0/Адоптедвхитепоинт. Y.</span><span class="sxs-lookup"><span data-stu-id="5645e-233">The scaling factor is 100.0/adoptedWhitePoint.Y.</span></span> <span data-ttu-id="5645e-234">Один и тот же коэффициент масштабирования применяется к каждому из X, Y и Z. Если поле Нормализетомедиавхитепоинт имеет значение «true» или отсутствует в CAMP, то механизм также масштабирует все входные цвета устройства в Девицетоколориметрик, чтобы значение Y белой точки носителя устройства совпадало с 100,0.</span><span class="sxs-lookup"><span data-stu-id="5645e-234">The same scaling factor is applied to each of X, Y, and Z. If the NormalizeToMediaWhitePoint field is set to "True," or if it is absent from the CAMP, the engine also scales all device colors input to DeviceToColorimetric so that the Y value of the device media white point equals 100.0.</span></span> <span data-ttu-id="5645e-235">Цвета устройств, поступающие из Колориметриктодевице, будут масштабироваться по мультипликативные в обратном масштабе этого коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="5645e-235">Device colors coming from ColorimetricToDevice will be scaled by the multiplicative inverse of that scaling factor.</span></span> <span data-ttu-id="5645e-236">Если для флага Нормализетомедиавхитепоинт задано значение false, то данные не масштабируются.</span><span class="sxs-lookup"><span data-stu-id="5645e-236">If the NormalizeToMediaWhitePoint flag is set to "False," then the colorimetric data is not scaled.</span></span>

<span data-ttu-id="5645e-237">Для некоторых задач имеет смысл масштабировать значения, поступающие от Девицетоколориметрик.</span><span class="sxs-lookup"><span data-stu-id="5645e-237">For some tasks, it makes sense to scale the colorimetric values coming from DeviceToColorimetric.</span></span> <span data-ttu-id="5645e-238">Гиперболические освещение на белой панели на самом деле разработаны для светимости белого цвета 100,0.</span><span class="sxs-lookup"><span data-stu-id="5645e-238">The hyperbolic lightness equations in the CAM are really designed for a white point luminance of 100.0.</span></span> <span data-ttu-id="5645e-239">Единственное место, где происходит разница в абсолютной освещенности (или иллуминанце), зависит от освещенности поля адаптации.</span><span class="sxs-lookup"><span data-stu-id="5645e-239">The only place where a difference in the absolute luminance (or illuminance) comes into play is in the luminance of the adapting field.</span></span> <span data-ttu-id="5645e-240">Таким образом, Камера должна быть инициализирована с белой точкой Y из 100,0.</span><span class="sxs-lookup"><span data-stu-id="5645e-240">So the CAM must be initialized with a white point Y of 100.0.</span></span> <span data-ttu-id="5645e-241">Но если в качестве принятой белой точки используется средняя точка в модели устройства, все цвета, поступающие от устройства, должны масштабироваться соответствующим образом, или белый список устройств не будет иметь значение J 100,0.</span><span class="sxs-lookup"><span data-stu-id="5645e-241">But if the device model's medium white point is being used as the adopted white point, then all colors coming from the device must be scaled accordingly, or device white will not come out with a J value of 100.0.</span></span> <span data-ttu-id="5645e-242">Поэтому значения Y должны масштабироваться в измерениях.</span><span class="sxs-lookup"><span data-stu-id="5645e-242">So the Y values have to be scaled in the measurements.</span></span> <span data-ttu-id="5645e-243">Значения измерений можно масштабировать до инициализации модели устройства.</span><span class="sxs-lookup"><span data-stu-id="5645e-243">The measurement values could be scaled before initializing the device model.</span></span> <span data-ttu-id="5645e-244">Затем результаты уже будут находиться в правильном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="5645e-244">Then results would already be in the proper range.</span></span> <span data-ttu-id="5645e-245">Но это может усложнить тестирование модели устройства, так как поступающие значения требуют масштабирования.</span><span class="sxs-lookup"><span data-stu-id="5645e-245">But that would make testing the device model more difficult, because the values coming out would require scaling.</span></span> <span data-ttu-id="5645e-246">Для задач, в которых средняя белая точка устройства считается истинным белым, желательно нормализацию с помощью белой точки носителя устройства.</span><span class="sxs-lookup"><span data-stu-id="5645e-246">For tasks in which the device medium white point is perceived to be a true white, normalizing by the device media white point is desirable.</span></span>

<span data-ttu-id="5645e-247">Камера инициализируется непосредственно из CAMP.</span><span class="sxs-lookup"><span data-stu-id="5645e-247">The CAM is initialized directly from the CAMP.</span></span> <span data-ttu-id="5645e-248">Это позволяет разработчикам гибко выполнять инициализацию, основываясь на задаче, которую они хотят выполнить.</span><span class="sxs-lookup"><span data-stu-id="5645e-248">This allows developers some flexibility in initializing the CAM, based upon the task they want to perform.</span></span> <span data-ttu-id="5645e-249">В некоторых задачах наблюдатели игнорируют любые чрома в белых точках мультимедиа, так как они ясно узнают, что исходный и конечный носители являются белыми.</span><span class="sxs-lookup"><span data-stu-id="5645e-249">In some tasks, observers will ignore any chroma in the media white points, because they cognitively "know" that the source and destination media are "white."</span></span> <span data-ttu-id="5645e-250">В таких случаях разработчикам нужно будет инициализировать прямую и обратную видеорегистраторов с соответствующими белыми точками мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5645e-250">In such cases, developers will want to initialize the forward and inverse CAMs with their respective media white points.</span></span> <span data-ttu-id="5645e-251">В некоторых случаях наблюдатели могут сравнивать цвет фона мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5645e-251">In some cases, observers may be comparing the color of the media backgrounds.</span></span> <span data-ttu-id="5645e-252">В таких случаях рекомендуется использовать одну и ту же шкалу для обоих устройств, и, возможно, нежелательно, чтобы масштабировать значения для каждого устройства на среднем белом месте.</span><span class="sxs-lookup"><span data-stu-id="5645e-252">In these cases, it is advisable to use one CAM for both devices, and it may be desirable not to scale each device's colorimetric values by that device's medium white point.</span></span> <span data-ttu-id="5645e-253">Затем различные значения тристимулус мультимедиа приведут к различным значениям внешнего вида в CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="5645e-253">Then the different tristimulus values of the media will lead to different appearance values in CIECAM02.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5645e-254">См. также</span><span class="sxs-lookup"><span data-stu-id="5645e-254">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5645e-255">Основные понятия управления цветом</span><span class="sxs-lookup"><span data-stu-id="5645e-255">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="5645e-256">Схемы и алгоритмы цветовой системы Windows</span><span class="sxs-lookup"><span data-stu-id="5645e-256">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





