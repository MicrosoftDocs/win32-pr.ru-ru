---
description: Метод Саурцелистфорцересолутион очищает последнее использованное свойство Source.
ms.assetid: 9ecfdf6e-4fed-46fc-8956-85d20cbe5327
title: Метод PATCH. Саурцелистфорцересолутион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f9a44d08c05b4ece24cf3c8c8d3be42e210aec32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651707"
---
# <a name="patchsourcelistforceresolution-method"></a>Метод PATCH. Саурцелистфорцересолутион

Метод **саурцелистфорцересолутион** очищает последнее использованное свойство Source. При этом установщик будет выполнять поиск допустимого источника исправления в списке источников, если в следующий раз требуется источник исправления. Например, установщик требует, чтобы источник обновления выполнил установку или переустановку, если отсутствует копия локального кэша обновления. Этот метод вызывает [**мсисаурцелистфорцересолутион**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).

## <a name="syntax"></a>Синтаксис


```JScript
Patch.SourceListForceResolution()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Защиты**](patch-object.md)
</dt> <dt>

[**мсисаурцелистфорцересолутион**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




