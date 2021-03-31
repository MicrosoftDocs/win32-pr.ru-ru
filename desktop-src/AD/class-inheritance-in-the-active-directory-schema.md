---
title: Наследование классов в схеме Active Directory
description: Все классы объектов в схеме службы Active Directory Directory являются производными от специального класса Top.
ms.assetid: 26e5107f-8204-4f64-bd07-b5b4f16103f4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd550a3eed6aeb633f6db265260b6c65c17f993
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069810"
---
# <a name="class-inheritance-in-the-active-directory-schema"></a>Наследование классов в схеме Active Directory

Все классы объектов в схеме службы Active Directory Directory являются производными от специального класса [**Top**](/windows/desktop/ADSchema/c-top). За исключением **Top**, все классы объектов являются подклассами другого класса Object. Например, [**Contact**](/windows/desktop/ADSchema/c-contact) является подклассом [**организатионалперсон**](/windows/desktop/ADSchema/c-organizationalperson); **организатионалперсон** является подклассом [**человека**](/windows/desktop/ADSchema/c-person); и **Person** — подкласс **Top**. Атрибут [**списках subClassOf**](/windows/desktop/ADSchema/a-subclassof) объекта [**classSchema**](/windows/desktop/ADSchema/c-classschema) является свойством с одним значением, указывающим на непосредственный суперкласс класса.

Некоторые значения атрибутов, определяющие класс, наследуются от его классов. Поэтому класс [**Contact**](/windows/desktop/ADSchema/c-contact) наследует значения от своих классов, которые являются классами [**организатионалперсон**](/windows/desktop/ADSchema/c-organizationalperson), [**Person**](/windows/desktop/ADSchema/c-person)и [**Top**](/windows/desktop/ADSchema/c-top) . Класс наследует следующие данные от своих классов:

-   Возможные атрибуты. значения атрибутов [**mustContain**](/windows/desktop/ADSchema/a-mustcontain), [**mayContain**](/windows/desktop/ADSchema/a-maycontain), [**системмустконтаин**](/windows/desktop/ADSchema/a-systemmustcontain)и [**системмайконтаин**](/windows/desktop/ADSchema/a-systemmaycontain) объекта [**classSchema**](/windows/desktop/ADSchema/c-classschema) определяют полный список атрибутов, которые могут быть установлены для экземпляра класса Object. Для каждого класса объектов значения этих атрибутов включают все значения, унаследованные от его классов, а также любые значения, явно заданные для самого класса объекта. Таким образом, атрибут [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) класса [**организатионалперсон**](/windows/desktop/ADSchema/c-organizationalperson) включает все значения **mustContain** , унаследованные от класса [**Person**](/windows/desktop/ADSchema/c-person) и [**ведущих**](/windows/desktop/ADSchema/c-top) классов, а также любые значения **mustContain** , явно заданные в классе **организатионалперсон** .
-   Возможные родители в иерархии каталогов: значения атрибутов [**possSuperiors**](/windows/desktop/ADSchema/a-posssuperiors) и [**системпосссупериорс**](/windows/desktop/ADSchema/a-systemposssuperiors) объекта [**classSchema**](/windows/desktop/ADSchema/c-classschema) определяют полный список классов объектов, которые могут содержать экземпляр класса Object. Для каждого класса объектов значения включают те, которые унаследованы от его классов, а также явно заданы для самого класса объекта.

Имейте в виду, что класс Object также может иметь много вспомогательных классов, которые указаны в атрибутах [**auxiliaryClass**](/windows/desktop/ADSchema/a-auxiliaryclass) и [**системауксилиарикласс**](/windows/desktop/ADSchema/a-systemauxiliaryclass) объекта **classSchema** . Класс объекта наследует значения [**mustContain**](/windows/desktop/ADSchema/a-mustcontain), [**mayContain**](/windows/desktop/ADSchema/a-maycontain), [**системмустконтаин**](/windows/desktop/ADSchema/a-systemmustcontain)и [**системмайконтаин**](/windows/desktop/ADSchema/a-systemmaycontain) из вспомогательных классов.

 

 