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
ms.openlocfilehash: a02e538a1d61fb0adf081542f10dea29f2a636e36b9ce936d7d282e30823339d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065864"
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
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик 3,0 или более поздней версии на Windows Server 2003, Windows XP и Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Обновление**](patch-object.md)
</dt> <dt>

[**мсисаурцелистфорцересолутион**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




