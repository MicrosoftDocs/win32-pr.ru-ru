---
description: 'Проверять орфографию в тексте поставщика более тщательно, чем Испеллчеккпровидер:: Check.'
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: 'Метод Икомпрехенсивеспеллчеккпровидер:: Компрехенсивечекк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IComprehensiveSpellCheckProvider.ComprehensiveCheck
api_type:
- COM
api_location:
- spellcheckprovider.h
ms.openlocfilehash: d999a90166e0d54d537abc84c30f6c4e0ee3768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684615"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a>Метод Икомпрехенсивеспеллчеккпровидер:: Компрехенсивечекк

Проверять орфографию в тексте поставщика более тщательно, чем [**испеллчеккпровидер:: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*текстовая надпись* \[ окне\]
</dt> <dd>

Проверяемый текст.

</dd> <dt>

*результат* \[ заполняет\]
</dt> <dd>

Результат проверки этого текста в виде перечисления орфографических ошибок ([**иенумспеллинжеррор**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), если таковые имеются.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Возвращаемое значение                                                                             | Описание                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>\_ОК</dt> </dl>         | Удалось.<br/>                |
| <dl> <dt>E \_ INVALIDARG</dt> </dl> | *текст* представляет собой пустую строку.<br/> |
| <dl> <dt>\_указатель E</dt> </dl>    | *текст* является пустым указателем.<br/>  |



 

## <a name="remarks"></a>Комментарии

Этот интерфейс не обязательно должен быть реализован поставщиком проверки орфографии. Но если поставщик поддерживает два режима проверки орфографии (более быстрый и медленный, но более тщательный), он должен реализовать этот интерфейс в том же объекте, который реализует [**испеллчеккпровидер**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) для поддержки более тщательного режима проверки. Когда клиент вызывает [**испеллчеккер:: компрехенсивечекк**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), функция проверки орфографии [**будет**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) возвращать поставщик для [**Икомпрехенсивеспеллчеккпровидер**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)и вызывать **икомпрехенсивеспеллчеккпровидер. ComprehensiveCheck** , если интерфейс поддерживается. Если интерфейс не поддерживается, он будет автоматически возвращаться к [**испеллчеккпровидер:: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**икомпрехенсивеспеллчеккпровидер**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)
</dt> <dt>

[**иенумспеллинжеррор**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)
</dt> <dt>

[**Испеллчеккер:: Компрехенсивечекк**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)
</dt> <dt>

[**испеллчеккпровидер**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider)
</dt> <dt>

[**Испеллчеккпровидер:: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
