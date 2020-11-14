<template>
  <div class="faq-wrapper">
    <b-container>
      <div class="context-faq">
        <h3>{{ txt.titleFaq }}</h3>
        <p>{{ txt.subTitleFaq }}</p>
      </div>
      <div class="table-faq">
        <div class="question-faq">
          <h5>{{txt.question}}</h5>
          <p>{{txt.subQuestion}}</p>
        </div>
        <div class="parent-answer">
          <div v-for="item in answers" :key="item.id" class="answer-faq">
            <h5>{{item.answer}}</h5>
            <font-awesome-icon  size="2x" icon="plus" />
          </div>
        </div>
      </div>
    </b-container>
  </div>
</template>

<script>
export default {
  name: "Faq",
  data() {
    return {
      txt: {
        titleFaq: 'Frequently asked questions',
        subTitleFaq: "The rise of mobile devices transforms the way we consume information entirely and the world's most elevant channels such as Facebook.",
        question: 'How to contact with riders emergency?',
        subQuestion: "Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition. Organically grow the holistic world view of disruptive innovation via workplace diversity and empowerment. Bring to the table win-win survival strategies to ensure proactive domination. At the end of the day, going forward, a new normal that has evolved from generation X is on the runway heading towards a streamlined cloud solution. User generated content in real-time will have multiple touchpoints for offshoring."
      },
      answers:[
        {
          id:1,
          answer:'App installation failed, how to update system information?'
        },
        {
          id:2,
          answer:'Website reponse taking time, how to improve?'
        },
        {
          id:3,
          answer:'New update fixed all bug and issues'
        },
        {
          id:4,
          answer:'How to contact with riders emergency?'
        }
      ]
    }
  }
}
</script>

<style scoped>
.faq-wrapper {
  padding: 5% 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

h3, h5 {
  color: #242f51;
  font-weight: bold;
}

p {
  color: #616368;
}

.context-faq {
  max-width: 650px;
  display: inline-block;
}

.context-faq p {
  padding: 1.5rem 0;
}

.table-faq {
  max-width: 940px;
  background-color: #f5f7fa;
  display: inline-flex;
  flex-direction: column;
}
.table-faq h5, .table-faq p {
  text-align: left;
}
.question-faq {
  padding: 2rem;
}
.answer-faq {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.answer-faq {
  padding: 0.5rem 2rem;
  border-top: 10px solid white;
}
</style>
